try and compare `google.golang.org/grpc` and `connectrpc.com/connect`

## setup

```console
$ go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
$ go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest
$ go install github.com/bufbuild/buf/cmd/buf@latest
$ go install github.com/bufbuild/connect-go/cmd/protoc-gen-connect-go@latest
```

## run

run server/client using grpc generated codes.

```console
$ go run ./cmd/server/grpc/main.go
$ go run ./cmd/client/grpc/main.go
```

run server/client using connect generated codes.

```console
$ go run ./cmd/server/connect/main.go
$ go run ./cmd/client/connect/main.go
```

run web client using conenct-web generated codes.

```console
$ cd web
$ npm run dev
```

## build

grpc

```console
$ cd api/grpc
$ protoc --go_out=../../gen --go_opt=paths=source_relative --go-grpc_out=../../gen --go-grpc_opt=paths=source_relative hello/v1/hello.proto
```

connect

```console
$ buf generate
```

## refs

- https://grpc.io/docs/languages/go/quickstart/
- https://zenn.dev/hsaki/books/golang-grpc-starting
- https://connectrpc.com/docs/go/getting-started/
- https://connectrpc.com/docs/web/getting-started/