`GOPATH` bug repro
==================

Steps:

1. Open this repo in a Codespace
2. Try to run `mkcert`, which is installed with `go install` in the `postCreateCommand`.

If you `echo $PATH`, you'll see that the `$GOPATH/bin` directory (`/go/bin`) isn't part of the PATH.