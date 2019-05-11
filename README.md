
pre-commit-golang
=================

golang hooks for http://pre-commit.com/

### Using these hooks

Add this to your `.pre-commit-config.yaml`

    - repo: git://github.com/dnephin/pre-commit-golang
      rev: master
      hooks:
        - id: go-fmt
        - id: go-lint
        - id: validate-toml
        - id: golangci-lint
        - id: go-unit-tests
        - id: go-build

### Available hooks

- `go-fmt` - Runs `gofmt`, requires golang
- `go-lint` - Runs `golint`, requires https://github.com/golang/lint
- `validate-toml` - Runs `tomlv`, requires
   https://github.com/BurntSushi/toml/tree/master/cmd/tomlv
- `golangci-lint` - run `golangci-lint run ./...`, requires
  [golangci-lint](https://github.com/golangci/golangci-lint)
- `go-unit-tests` - run `go test -tags=unit -timeout 30s -short -v`
- `go-build` - run `go build`, requires golang
