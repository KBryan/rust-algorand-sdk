# rust-algorand-sdk

# Documentation

General Algorand documentation is available at https://developer.algorand.org/
This is the current attempt to stay up Rust version of the Algorand SDK

# Quickstart

```rust
use algosdk::{AlgodClient, KmdClient};

fn main() {
    let algod_address = "http://localhost:4001";
    let algod_token="aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa";
    let kmd_address = "http://localhost:4002";
    let kmd_token = "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa";

    let algod_client = AlgodClient::new(algod_address, algod_token);
    let kmd_client = KmdClient::new(kmd_address, kmd_token);

    println!("Algod versions: {:?}", algod_client.versions().unwrap().versions);
    println!("Algod status: {:?}", algod_client.status().unwrap());

    println!("Kmd versions: {:?}", kmd_client.versions().unwrap().versions);
    println!("Kmd status: {:?}", kmd_client.status().unwrap().versions);

}
```
