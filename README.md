[README-2.md](https://github.com/user-attachments/files/27214201/README-2.md)

# MannaSeed

**Hidden Provision. Eternal Word.**

MannaSeed is an open source project with two components:

1. **The Blockchain Bible** — the complete King James Bible permanently inscribed on Bitcoin's base layer as 66 individual Ordinal inscriptions, one per book. Live at [blockchainbible.org](https://blockchainbible.org).

2. **The App** — a calculator-disguised offline Bible reader that decrypts the complete KJV entirely in device memory, leaving no trace on the device when the session ends. Built for believers in environments where carrying scripture is a legal risk.

---

## The Blockchain Bible

All 66 books of the King James Bible were inscribed on Bitcoin mainnet between April 22–25, 2026. Each inscription is a real Bitcoin transaction — confirmed, immutable, and independently verifiable by anyone with the transaction ID.

- **Read it:** [blockchainbible.org/Read](https://blockchainbible.org/Read)
- **Verify it:** [blockchainbible.org/Verify](https://blockchainbible.org/Verify)
- **Full inscription data:** see `INSCRIPTIONS.csv`

To verify any inscription independently, take any TxID from `INSCRIPTIONS.csv`, fetch the content at `https://ordinals.com/content/<txid>i0`, and compute its SHA-256 hash. Compare against the `sha256_verified` column. No trust in this project required — the math speaks for itself.

---

## The App

The MannaSeed app is a contingency — software that lets a believer carry the complete King James Bible through any checkpoint, on any device, leaving no trace that any forensic tool can find.

- Disguised as a fully functional calculator
- Bible decrypts from AES-256-GCM encrypted binary into device RAM only
- Zero network requests — fully offline at all times
- Kill switch: power button clears memory instantly
- BIP39 seed phrase authentication
- Three decoy methods — journal opens under duress, Bible stays protected
- 60-second idle timeout with automatic session termination

**Status:** In development. Phase 0 (blockchain inscriptions) is complete. Phase 1 (HTML file) is next.

Full design specification in the [whitepaper](MannaSeed_Whitepaper_v1_3.pdf).

---

## Repository Contents

| File | Description |
|---|---|
| `INSCRIPTIONS.csv` | All 66 TxIDs with verification data |
| `MannaSeed_Whitepaper_v1_3.pdf` | Full project whitepaper |

---

## Verify It Yourself

Every inscription is publicly verifiable. To verify a single book manually:

1. Find its TxID in `INSCRIPTIONS.csv`
2. Go to `https://ordinals.com/content/<txid>i0`
3. Compute SHA-256 of the returned content
4. Compare against `sha256_verified` in `INSCRIPTIONS.csv`

If the hashes match, the on-chain content is byte-for-byte identical to the source. No trust required.

---

## License

MIT License. Free forever. The Bible text is public domain. The cryptography is standard. Fork it, copy it, improve it.

There is no paid version. There is no premium tier. Profiting from the Word of God is wrong.

---

*"The grass withers and the flowers fall, but the word of our God endures forever."*
— Isaiah 40:8

**Open Source · Free Forever · [blockchainbible.org](https://blockchainbible.org)**
