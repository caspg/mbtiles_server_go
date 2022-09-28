Reading mbtiles metadata:

```bash
sqlite3 poland-bicycle-infra.mbtiles
```

```SQL
select * from metadata where name is not 'json';
```

## Building

Building for ubuntu from mac

```bahs
# https://github.com/mattn/go-sqlite3#cross-compiling-from-mac-osx
brew install FiloSottile/musl-cross/musl-cross
```

```bash
CC=x86_64-linux-musl-gcc CXX=x86_64-linux-musl-g++ GOARCH=amd64 GOOS=linux CGO_ENABLED=1 go build -ldflags "-linkmode external -extldflags -static"
```

## Systemd

1. Copy `mbtiles_server_go.service` to `/lib/systemd/system`
2.
