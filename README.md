# Iron Sun Open OS

**Local-first stewardship software.** A personal and organizational record that lives entirely on your device.

> Honor what came before. Care for what is here. Leave more behind than we received.

Iron Sun Open OS is a single-file web app for keeping a meaningful, tamper-evident record of the actions you take as a steward — across whatever roles matter to you. It runs offline, stores nothing on any server, and asks nothing of the cloud.

## What it is

- **Local-first.** Your records are kept on your device, in your browser's storage. Nothing is uploaded.
- **Append-only.** Records are added, never edited in place. Corrections become new links.
- **Hash-chained.** Each record carries the cryptographic hash of the one before it, so accidental corruption is detectable.
- **Offline.** No server, no cloud, no network dependency. Works on a plane.
- **Yours.** Export your full ledger to a file at any time; import it back to restore.
- **Open source.** Released under the MIT License.

## What it is not

By deliberate design, Iron Sun Open OS contains:

> no token · no coin · no payment · no custody · no marketplace · no value transfer · no prediction · no diagnosis · no ranking · no spiritual authority

It is a stewardship record, not a financial instrument, an oracle, or a scoring system. The Observatory reflects your own records and factual time/season context back to you — it does not predict, score, diagnose, rank, or claim authority.

## A note on the hash chain

The chain is **tamper-evident**, not tamper-proof. It reliably detects casual corruption or an edit that doesn't recompute later hashes. It does **not** prove authorship or authenticity, because there are no signing keys — anyone with the file can, in principle, rewrite a record and recompute the chain. Treat it as an integrity check on your own records, not as cryptographic proof of provenance.

## Running it

**On a phone (simplest):** open `index.html` in a mobile browser (Safari on iPhone), then use Share → Add to Home Screen.

**As an installable app (offline):** host the files on any static host with https (e.g. GitHub Pages) and open the link. The browser will offer to install it; once installed it runs fully offline.

**Locally:** open `index.html` directly in a browser. Everything works except the offline-install (service worker), which needs https.

## Backing up

Records live in browser storage, which a browser can clear. Use the **Export** tab to download your ledger as JSON now and then. **Import** restores it — and verifies the chain before replacing anything, refusing a corrupted backup.

## Files

- `index.html` — the entire application
- `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png` — installable-app support
- `LICENSE` — MIT

## License

MIT © 2026 Gary William Oakley Jr. See `LICENSE`.
