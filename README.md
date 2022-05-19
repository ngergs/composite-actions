# Github actions collection

My personal collection of composite GitHub Actions for personal use.

The composite actions are aimed at simplicity and do not offer full customizable compared to their individual components.

## Content
* go-test: Runs test for a go application using go test ./...
* prepare-semantic-release: Determines the next version number using [go-semantic-release/action@v1](https://github.com/go-semantic-release/action) and stored the release notes in a [actions/cache@v3](https://github.com/actions/cache).
* release-docker: Builds a docker container, pushes it to DockerHub and creates a GitHub release using [softprops/action-gh-release@v1](https://github.com/softprops/action-gh-release)
* release-go-binary: Builds a go binary and attaches it to a GitHub release created using [softprops/action-gh-release@v1](https://github.com/softprops/action-gh-release)
## Caching
Go modules are cached using the GitHub Action [actions/cache@v3](https://github.com/actions/cache) and the key 
```
${{ runner.os }}-go-${{ hashFiles('**/go.sum') }}
```