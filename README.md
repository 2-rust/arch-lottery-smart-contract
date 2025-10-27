# Arch Lottery

**Arch Lottery** is a local development stack for the **Arch Network**, featuring a sample **Lottery smart contract**. This project helps developers experiment with Arch Network transactions, UTXO handling, and smart contract execution in a test environment.

---

## **Requirements**

Before getting started, ensure you have the following installed:

- **Rust** (latest stable version)
- **Docker** (for local Arch Network deployment)
- **C++ Compiler** (`gcc` or `clang`)
- **Solana CLI** (for Solana-compatible tooling)

> ⚡ *Optional:* You can use VS Code or another IDE for Rust development and debugging.

---

## **Getting Started**

The Arch Lottery example demonstrates a simple **Raffle smart contract** on the Arch Network.
You can also explore the smart contract code here: [arch-lottery-smart-contract/examples/raffle](https://github.com/2-rust/arch-lottery-smart-contract/tree/master/examples/raffle)

### Steps:

1. **Clone the repository**
```bash
git clone https://github.com/2-rust/arch-lottery.git
cd arch-lottery
```

2. **Build the Lottery program**
```bash
cargo build-sbf
```
This compiles the Rust smart contract into **SBF (Solana Binary Format)** for local execution.

3. **Run tests / execute transactions**
```bash
# Return to the raffle directory and run test
cd .. && cargo test -- --nocapture
```
This simulates a lottery transaction on the **local Arch Network**, showing program execution, account updates, and UTXO handling.

---

## **Project Structure**
```
arch-lottery/
├─ examples/raffle/        # Sample lottery smart contract
├─ local-network/          # Scripts for spinning up local Arch testnet
├─ Cargo.toml              # Rust project configuration
└─ README.md               # Documentation
```

---

## **How It Works**

- **Lottery Smart Contract:** Handles entry, winner selection, and payout logic.
- **Arch Network Local Stack:** Simulates blockchain environment locally using Docker and Rust programs.
- **UTXO Model:** Each transaction updates unspent outputs, ensuring accurate state management.

---

## **Next Steps**

1. Modify the **raffle smart contract** to add custom logic (e.g., weighted entries, multiple winners).
2. Experiment with **transactions** on the local network.
3. Integrate **frontend or CLI** to interact with the Lottery smart contract.
4. Deploy on a **testnet** when ready.
