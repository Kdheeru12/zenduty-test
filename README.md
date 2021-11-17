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
Configure the Token and Url

```
config := &client.Config{
	Token: "", // enter token for authentication
	BaseURL: "", // your url 
	}
```
Based on the service you want to communicate with,Create object for required class,For example, to create Team



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

	newteam := &client.Team{}
	newteam.Name = "test"

	resp, err := c.Teams.CreateTeam(newteam)
	if err != nil {
		panic(err)
	}
	fmt.Printf("%+v\n", resp)

}


```

