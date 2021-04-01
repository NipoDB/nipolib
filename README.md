GO library for nipo .

# sample

    package main

    import (
    	"github.com/NipoDB/nipolib"
    	"fmt"
    )

    func main() {
        config := nipolib.CreateConfig("TOKEN", "IP of SERVER", "PORT")
        SetResult,Setok := nipolib.Set(config, "KEY", "VALUE")
        if !Setok {
            fmt.Println("Error at set")    
        } else {
            fmt.Println("Set OK")
            fmt.Println(SetResult)
        }

        GetResult,Getok := nipolib.get(config, "KEY")
        if !Getok {
            fmt.Println("Error at get")    
        } else {
            fmt.Println("get OK")
            fmt.Println(GetResult)
        }
    }
    