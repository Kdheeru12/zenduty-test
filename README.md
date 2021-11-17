# zenduty-go-sdk
 

## Example usage
```go
package main

import (
	"fmt"
	"github.com/zenduty/go-sdk"
)

func main() {
	config := &client.Config{
		Token: "", // enter token for authentication
	}

	c, err := client.NewClient(config)
	if err != nil {
		panic(err)
	}
	resp, err := c.Teams.GetTeams()
	if err != nil {
		panic(err)
	}
	fmt.Printf("%+v\n", resp)

}

```

