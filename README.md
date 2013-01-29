gosnow
======

snowflake in golang

This fork replaces the the usage of panic() by returning errors instead.

~~~golang
package main

import (
    "github.com/sdming/gosnow"
    "fmt"
)

func main() {

    v,err := gosnow.Default()
    //v, err := gosnow.NewSnowFlake(100)
    for i := 0; i < 10; i++ {
        id, err := v.Next()
        fmt.Println(id)
    }
}

~~~