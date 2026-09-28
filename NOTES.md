# Codama Assignment Notes

## Tool Versions

- Anchor CLI: 1.1.2
- Solana CLI: 3.1.10
- Node.js: v24.10.0
- Codama: 1.6.3

## PDA Account Resolution

In `contribute`, the `fundraiser` PDA uses the seeds `"fundraiser"` and `fundraiser.maker`. Since `maker` is a field inside the fundraiser account itself, it cannot be used to derive the fundraiser address before the account has been found, so `fundraiser` must be supplied explicitly.

In `initialize`, the fundraiser PDA instead uses `"fundraiser"` and the explicit `maker` account, so Codama can derive the fundraiser address from the available inputs. In `contribute`, Codama can derive `contributorAccount` and `contributorAta` because their seeds can be resolved from accounts already available to the instruction.