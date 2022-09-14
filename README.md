`GOPATH` bug repro
==================

Steps:

1. Clone the repo and open it in VS Code
2. Run "Rebuild and Reopen in Container"
2. Try to run `mkcert`, which is installed with `go install` in the `postCreateCommand`.

If you `echo $PATH`, you'll see that the `$GOPATH/bin` directory (`/go/bin`) isn't part of the PATH.
