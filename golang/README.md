# golang

```sh
# golangディレクトリごとコピー。

export MODULE_PATH=github.com/2754github/foo
export GO_VERSION=1.27.2
export LINTER_VERSION=2.14.0

mkdir -p .vscode
envsubst '$MODULE_PATH $GO_VERSION $LINTER_VERSION' < golang/.golangci.yaml > .golangci.yaml
envsubst '$MODULE_PATH $GO_VERSION $LINTER_VERSION' < golang/.vscode/settings.json > .vscode/settings.json
envsubst '$MODULE_PATH $GO_VERSION $LINTER_VERSION' < golang/Containerfile > Containerfile
envsubst '$MODULE_PATH $GO_VERSION $LINTER_VERSION' < golang/mise.toml > mise.toml

mise install
go mod init $MODULE_PATH
go get -tool golang.org/x/tools/cmd/deadcode@latest
go get -tool golang.org/x/vuln/cmd/govulncheck@latest
```

- [Recommended settings for those who installed golangci-lint via extension](https://golangci-lint.run/docs/welcome/integrations/)
- [Configuration File](https://golangci-lint.run/docs/configuration/file/)
- <https://github.com/GoogleContainerTools/distroless/blob/main/examples/go/Dockerfile>
- <https://github.com/golang/go/issues/64713>
