# Generate documentation for Bess

As opposed to the [official
documentation](https://github.com/NetSys/bess/wiki/Built-In-Modules-and-Ports),
this program generates documentation that

* lists every class method (dedicated protobuf message is not a
  requirement)

* links c++ defintions and usage examples.

# Execution steps

1. Clone or update bess repository,
1. Compile bess with container_build,
1. Extract documentation from protobuf messages,
1. Collect modules and their methods by running bessd in a container,
1. Find method definitions by running gdb,
1. Write a dummy module ([mclass.py](https://github.com/nemethf/pyls-bess/blob/master/pyls_bess/bess_doc/mclass.py)).

# Uninstall

To remove the software, you also need to remove some docker images.
```
$ docker image rm gen-bess-doc-mclass
$ docker image rm nefelinetworks/bess_build
$ docker image rm pseudomuto/protoc-gen-doc
```

# Is it any good?

At least the [bess language
server](https://github.com/nemethf/pyls-bess) uses it.
