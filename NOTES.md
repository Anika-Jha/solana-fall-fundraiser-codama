## Versions

anchor-cli 1.1.2 · node v24.10.0 · @codama/cli 1.6.3

## TODO 3

Required: fundraiser, vault. Optional: contributorAccount, contributorAta, tokenProgram, systemProgram.

`contribute` seeds the fundraiser PDA on `fundraiser.maker`, a field of the account being derived, so the finder would need the account to find the account. `initialize` seeds it on the `maker` account, which the caller has, so there it is optional.

## Bonus

attempted

## One thing that surprised me

The generated Codama client could reproduce Anchor's `contribute` instruction byte-for-byte, including the instruction data and account ordering, while also resolving several accounts automatically from the IDL's PDA and ATA definitions.
