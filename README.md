# osmshortlink-go: Go module and command-line tool for creating, encoding & decoding of OpenStreetMap shortlinks

[![Test](https://github.com/stefanb/osmshortlink-go/actions/workflows/test.yml/badge.svg)](https://github.com/stefanb/osmshortlink-go/actions/workflows/test.yml)
[![golangci-lint](https://github.com/stefanb/osmshortlink-go/actions/workflows/golangci-lint.yml/badge.svg)](https://github.com/stefanb/osmshortlink-go/actions/workflows/golangci-lint.yml)
[![CodeQL](https://github.com/stefanb/osmshortlink-go/actions/workflows/codeql.yml/badge.svg)](https://github.com/stefanb/osmshortlink-go/actions/workflows/codeql.yml)
[![Go Reference](https://pkg.go.dev/badge/github.com/stefanb/osmshortlink-go.svg)](https://pkg.go.dev/github.com/stefanb/osmshortlink-go)

Specification: https://wiki.openstreetmap.org/wiki/Shortlink

## Usage

### Creating a link in Go

```go
package main
import "github.com/stefanb/osmshortlink-go"

func main() {
    shortlink, err := osmshortlink.Create(46.05141, 14.50604, 17)
    if err != nil {
        panic(err)
    }
    fmt.Println(shortlink)
}
```

Prints: [`https://osm.org/go/0Ik3VNr_A-?m`](https://osm.org/go/0Ik3VNr_A-?m)

### Command-line tool

You can download pre-built binaries for various platforms from [latest release](https://github.com/stefanb/osmshortlink-go/releases/latest).

```bash
Usage: osmshortlink [latitude] [longitude] [zoom]
```

For example:

```bash
$ osmshortlink 46.05141 14.50604 17
https://osm.org/go/0Ik3VNr_A-?m
```
