# svd2json

Simple wrapper around the `svd2rust` crate which converts the SVD data to JSON format. Converted data is written to a file which has the same path as the input file, but with '.json' appended to the end of the filename.

Usage: `cargo run <file.svd>` - data gets written to 'file.svd.json'.

Note that this only works if the `svd` crate supports the `serde` crate's `Serialize` and `Deserialize` traits on the Rust structs. This project's `Cargo.toml` file assumes that a modified crate is located one directory up. You can find a modified version of the `svd` crate here, until/if those changes are merged upstream:

https://github.com/WRansohoff/svd
