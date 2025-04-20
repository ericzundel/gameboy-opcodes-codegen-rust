# gameboy-opcodes-codegen-rust

Transform Opcodes.json into a rust structure. Example of how to do code generation with quote!() macro in Rust

## Summary

This tool generates a file named gen_opcodes.rs.  This is a rust datastructure of some data that originated
in a .json file named Opcodes.json. See the original source of this data at
[gbdev.io](https://gbdev.io/gb-opcodes/optables/).

## How to use this tool

You will need rust toolchain and cargo installed.  Simply run

```bash
$ cargo run
```

from the root of this repo to regenerate gen_opcodes/gen_opcodes.rs

this code uses the `tracing` crate for logging.  To turn on tracing try:

```bash
$ RUST_LOG="trace,info,error" cargo run
```

## Notes

The code generator tries to pretty print gen_opcodes.rs using the prettyprint crate, but doesn't do a 
great job.  The checked in version was likely formatted with `rustfmt`.

