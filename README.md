```go
package main

import "bytes"
import example_ego "github.com/letusfly85/example_ego"

func main() {
    myUser := &my_ego.User{
        FirstName:      "Bob",
        FavoriteColors: []string{"blue", "green", "mauve"},
    }

    var buf bytes.Buffer
    if err := example_ego.MyTmpl(&buf, myUser); err != nil {
        panic(err)
    }
    println(buf.String())
}
```
