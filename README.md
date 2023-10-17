try and compare `google.golang.org/grpc` and `connectrpc.com/connect`

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

## refs

- https://zenn.dev/hsaki/books/golang-grpc-starting
- https://connectrpc.com/docs/go/getting-started/
- https://connectrpc.com/docs/web/getting-started/