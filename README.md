# Exploring NEAR

## Resources

- [cargo-near](https://github.com/near/cargo-near) - NEAR smart contract development toolkit for Rust
- [near CLI](https://near.cli.rs) - Interact with NEAR blockchain from command line
- [NEAR Rust SDK Documentation](https://docs.near.org/sdk/rust/introduction)
- [NEAR Documentation](https://docs.near.org)
- Rainbow bridge https://www.near.org/blog/eth-near-rainbow-bridge
- Aurora https://aurora.dev/

## Notes

- Compiles to wasm

- Tries to support reproducible builds

- Looks well-documented

- NEAR is deep into AI (as of Summer 2025)

- Concept of Virtual chains, EVM-compatible chains that run as smart contracts on NEAR, without the traditional L2 infrastructure

- NEAR has cross-chain capabilities, through chain abstraction

- NEAR has chain abstraction. NEAR's chain abstraction framework consists of three core technologies that work together to create seamless cross-chain experiences: NEAR intents, Chain signatures and OmniBridge.

- Chain Signatures enable NEAR accounts, including smart contracts, to sign and execute transactions across many blockchain protocols. By using Multi-Party Computation (MPC)

## Instructions

### With local installation

cargo near https://github.com/near/cargo-near :

```bash

# Install cargo near to help building the contract
curl --proto '=https' --tlsv1.2 -LsSf https://github.com/near/cargo-near/releases/latest/download/cargo-near-installer.sh | sh
```

Requirements: Rust >= 1.88.0 && cargo near

```bash
rustup target add wasm32-unknown-unknown
```

```bash
git clone https://github.com/Neal-C/exploring_near.git
```

```bash
cd exploring_near
```

```bash
cargo near build
```

## How to Build Locally?

Install `cargo-near`(https://github.com/near/cargo-near) and run:

```bash
cargo near build
```

## How to Deploy?

Deployment is automated with GitHub Actions CI/CD pipeline.
To deploy manually, install [`cargo-near`](https://github.com/near/cargo-near) and run:

If you deploy for debugging purposes:
```bash
cargo near deploy build-non-reproducible-wasm <account-id>
```

If you deploy production ready smart contract:
```bash
cargo near deploy build-reproducible-wasm <account-id>
```

