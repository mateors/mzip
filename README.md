# Zip unzip package

### How to install this package?
> go get github.com/mateors/mzip

### How to make zip files?
```go
package main

import "github.com/mateors/mzip"

func main(){

 //How to make zip
 isOk,err:=mzip.MakeZip("test", "output.zip")
 if err!=nil{
     fmt.Println(err.Error())
 }
 fmt.Println("zip created:", isOk)

  //How to unzip
 filesSlice,err:=mzip.Unzip("output.zip", "outputFolderName")
 if err!=nil{
     fmt.Println(err.Error())
 }
 fmt.Println("Total unzipped files:", len(filesSlice))

}
 
```
