# `rr`, aka `RestartReader`

`RestartReader` allows you to read bytes from an io.Reader without removing them.

`RestartReader` wraps `io.ReadCloser` or `io.Reader` and implements it. It holds the data from every `Read` in a buffer, and allows you to call `.Restart()`, causing subsequent `Read` calls to start from the beginning again. This is useful when you need to read the first few bytes of a stream or file, before passing off the full data to another function.

Import it with:

```go
go get github.com/makeworld-the-better-one/rr
```

## License

MIT
