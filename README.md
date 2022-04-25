# HelloWorld gRPC API

A sample to demonstrate how to separate gRPC API definition (`.proto` file) from the implementation code.

## Building

```console
$ cargo build
```

## Using from a project

Declare the dependency in `Cargo.tml`:
```toml
rust_hello_api = { version = "0.1.0", git = "../helloworld-api" }
```

or a local path:
```toml
rust_hello_api = { version = "0.1.0", git = "https://github.com/neeme-praks-sympower/helloworld-api" }
```

And then from your Rust server code:
```rust
use helloworld_lib::hello_world::greeter_server::{Greeter, GreeterServer};
use helloworld_lib::hello_world::{HelloReply, HelloRequest};
```

Or Rust client code:
```rust
use helloworld_lib::hello_world::greeter_client::GreeterClient;
use helloworld_lib::hello_world::HelloRequest;
```
