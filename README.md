# ChatWork API Client for Golang

[ChatWork](http://www.chatwork.com/) client for Golang.

## Install

```
$ go get github.com/eiel/go-chatwork
```

## Usage

```go
package main

import (
  chatwork "github.com/eiel/go-chatwork"
)

func main() {
  chatwork := chatwork.NewClient(`api-key`)

  chatwork.Me()

  chatwork.MyStatus()

  chatwork.MyTasks(map[string]string {
    "assigned_by_account_id": "123",
    "status": "open"
  })

  ...
}
```

### for GoogleAppEngine/Go

```go
c := appengine.NewContext(r)
client := urlfetch.Client(c)
chatwork := chatwork.NewClient(`api-key`)
chatwork.HttpClient = client
```

See more examples in `examples` directory.
