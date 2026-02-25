# Blueshift Anchor Vault

Completed the Blueshift Anchor Vault challenge. Simple escrow program on Solana using Anchor.

<img width="475" height="575" alt="Screenshot 2026-02-25 at 7 12 04 PM" src="https://github.com/user-attachments/assets/5c77a42a-f00a-4ed9-b30a-daf7c88fdd1f" />


## What it does

- Deposit SOL into a PDA vault
- Withdraw all SOL from the vault
- Each user gets their own vault derived from their pubkey

## Structure

- `deposit`: Transfer SOL from user to vault PDA
- `withdraw`: Transfer all SOL back to user and close vault
- Vault seeds: `["vault", user_pubkey]`

## Requirements

- Amount must be greater than rent-exempt minimum
- Can only deposit to empty vault
- Can only withdraw from existing vault

## Build

```bash
anchor build
```

## Test

```bash
anchor test
```

## Deploy

```bash
anchor deploy
```
