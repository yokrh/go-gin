# gin
A web framework for Go.
https://github.com/gin-gonic/gin

## Hello gin

```sh
# init project
go mod init `pwd`
ls

# install module
go get -u github.com/gin-gonic/gin

# create main file
touch main.go
```
```go
package main

import "net/http"
import "github.com/gin-gonic/gin"

func main() {
  r := gin.Default()
  r.GET("/ping", func(c *gin.Context) {
    c.JSON(200, gin.H{
      "message": "pong",
    })
  })
  r.Run() // listen and serve on 0.0.0.0:8080
}
```
```sh
# run the server
go run main.go
```

##

