# Overview of A Tokenizer Library

## Dependencies

* [A cmake library](https://github.com/knode-ai-open-source/a-cmake-library) needed for the cmake build
* [A memory library](https://github.com/knode-ai-open-source/a-memory-library) for the memory handling
* [The macro library](https://github.com/knode-ai-open-source/the-macro-library) for sorting, searching, and conversions
* [The IO library](https://github.com/knode-ai-open-source/the-io-library) for IO handling
* [The LZ4 Library](https://github.com/knode-ai-open-source/the-lz4-library) for compression

## Building

### Build and Install
```bash
mkdir -p build
cd build
cmake ..
make
sudo make install
```

### Uninstall
```bash

```

### Build Tests and Test Coverage
```bash
mkdir -p build
cd build
cmake BUILD_TESTING=ON ENABLE_CODE_COVERAGE=ON ..
make
ctest
make coverage
```

### Sample usage

See tests/src/parse.c and tests/src/parse_expression.c for sample usage.

Build tests
```bash
cd build
cmake BUILD_TESTING=ON ..
make
cd tests
```

Test an expression
```bash
$ ./parse_expression '(a OR b c d OR d) not "e g"'
not
	"
		e
		g
	(
		or
			a
			(
				b
				c
				d
			d
```

Test parsing this README file
```bash
$ ./parse ../../README.md
Overview
of
A
Template
Library
Building
Build
and
Install
```
