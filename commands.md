# Go Modules Commands

```sh
# init a module name example.com/hello
go mod init example.com/hello

# list the current module's dependencies
go list -m all

# list all minor and patch upgrades available for the current module's dependencies
go list -u -m all

# list all current module's dependencies matching a pattern
go list -m rsc.io/q...

# list all versions available for a module
go list -m -versions rsc.io/sampler

# upgrade a dependency to a specific version
go get rsc.io/sampler@v1.3.1

# for adding a new dependency, just import and run `go mod tidy`, `go build` or `go test`

# upgrade all dependencies (direct and indirect) to the latest minor and patch versions
go get -u ./...

# remove unused dependencies and fetch uninstalled dependencies and update go.mod and go.sum
# always run `go mod tidy` before committing a go.mod file to version control
go mod tidy

# find out why a version of a dependency is included
go mod why -m github.com/lib/pq
go mod graph | grep github.com/lib/pq

# vendoring dependencies
go mod vendor

# build or test all packages in the module
go build ./...
go test ./...

# tag a release and push to origin
git tag v0.1.0
git push origin v0.1.0

# tag a pre-release v2 version and push to origin
git tag v2.0.0-alpha.1
git push origin v2.0.0-alpha.1
```
