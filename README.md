## SGX

SGX project consists of two binaries: server and client. Server is expected to be executed 
in [Anjuna](https://anjuna.io) environment. Please, run these commands to see how they can be used:

```
cd ./pps-sgx
cargo run --bin server -- --help
cargo run --bin client -- --help
```

## Garbled circuits

There's a [test file](./pps-garbled-circuits/tests/circuits-usage.rs) that demonstrates usage 
of the library. It's extensively commented, so it should be a good place to get familiar with
the library.

The test file consist of three tests: update_table, update_index_table, batched_update_table;
each covers according use-case described in the paper. You can run them via following command:

```
cd ./pps-garbled-circuits
cargo test
```

Parameters (like size of table) are hardcoded. For instance, update_table uses [table size m=3 l=4]. 
You can simply edit this line, and recompile test in order to try different params.

[table size m=3 l=4]: https://github.com/ZenGo-X/pps-gc/blob/161d78b213e936ccca498e3432ac01f33378fe20/pps-garbled-circuits/tests/circuits-usage.rs#L22
