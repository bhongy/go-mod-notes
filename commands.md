# Go Modules Commands

```sh
# init a module name example.com/hello
go mod init example.com/hello

# list the current module's dependencies
go list -m all

# list all current module's dependencies matching a pattern
go list -m rsc.io/q...

# list all versions available for a module
go list -m -versions rsc.io/sampler

# upgrade a dependency to a specific version
go get rsc.io/sampler@v1.3.1

# for adding a new dependency, just import and run `go mod tidy`, `go build` or `go test`

# remove unused dependencies and fetch uninstalled dependencies
go mod tidy
```
