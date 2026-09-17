# Go

**Wickra ZK — for Go. `go get github.com/wickra-lib/wickra-zk-go` — over the C ABI via cgo, prebuilt library bundled in the module.**

```bash
go get github.com/wickra-lib/wickra-zk-go
```

```go
package main

import (
	"fmt"

	wickra "github.com/wickra-lib/wickra-zk-go"
)

func main() {
	p := wickra.New()
	defer p.Close()

	cmd := `{"cmd":"prove","spec":{"strategy":{...}},` +
		`"candles":[{"time":1,"open":100,"high":101,"low":99,"close":100,"volume":1000}]}`

	proof, err := p.Command(cmd)
	if err != nil {
		panic(err)
	}
	fmt.Println(proof) // {"receipt":…,"journal":{"report_hash":"…","dataset_commitment":"…","guest_id":"…",…},"version":"…"}
	fmt.Println(wickra.Version())
}
```

## More

- [pkg.go.dev](https://pkg.go.dev/github.com/wickra-lib/wickra-zk-go)
- [Source & examples](https://github.com/wickra-lib/wickra-zk/tree/main/examples/go)
