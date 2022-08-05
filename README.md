[![Tests on Linux, MacOS and Windows](https://github.com/bep/varexpand/workflows/Test/badge.svg)](https://github.com/bep/varexpand/actions?query=workflow:Test)
[![Go Report Card](https://goreportcard.com/badge/github.com/bep/varexpand)](https://goreportcard.com/report/github.com/bep/varexpand)
[![GoDoc](https://godoc.org/github.com/bep/varexpand?status.svg)](https://godoc.org/github.com/bep/varexpand)

This library has one Go func, `Expand`, which is similar to [os.Expand](https://pkg.go.dev/os#Expand) – with one major difference: It only considers `${var}`.

This may sound limiting, but `os.Expand` has lots of situations where it breaks, e.g. regular expressions.

Note that this implementation may also be slower than the stdlib variant (I will eventually add some benchmarks), so don't use it on William Shakespeare's complete works.