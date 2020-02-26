[![license](http://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/breiting/gwob/blob/master/LICENSE)
[![GoDoc](https://godoc.org/github.com/breiting/gwob?status.svg)](http://godoc.org/github.com/breiting/gwob)
[![Go Report Card](https://goreportcard.com/badge/github.com/breiting/gwob)](https://goreportcard.com/report/github.com/breiting/gwob)

**This is a fork of the [original gwob](http://github.com/udhos/gwob) library**

# gwob
gwob - Pure Go Golang parser for Wavefront .OBJ 3D geometry file format

# Usage

Import the package in your Go program:

    import "github.com/breiting/gwob"

Example:

    // Error handling omitted for simplicity.

    import "github.com/udhos/gwob"

    options := &gwob.ObjParserOptions{} // parser options

    o, errObj := gwob.NewObjFromFile("gopher.obj", options) // parse/load OBJ

    // Scan OBJ groups
    for _, g := range o.Groups {
        // ...
    }

# Example

Run the example:

    cd example
    go run main.go

You can supply a custom input OBJ by setting the env var INPUT:

    INPUT=gopher.obj go run main.go

If you specify any command line argument, the OBJ will be dumped to stdout:

    go run main.go d

See directory [example](example).

# Documentation

See the [GoDoc](http://godoc.org/github.com/breiting/gwob) documentation.
