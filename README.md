# zenduty-go-sdk
 Zenduty API client in Go, primarily used by [Zenduty](https://github.com/Kdheeru12/terraform-zenduty) provider in Terraform.
 
 ## Installation
```bash
go get github.com/Kdheeru12/zenduty-test/client
```


## Getting started
Before you begin making use of the SDK, make sure you have your Zenduty Access Token.

```
import "github.com/Kdheeru12/zenduty-test/client"

```

## Example usage
```go
package main

import (
	"fmt"

	"github.com/Kdheeru12/zenduty-test/client"
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

