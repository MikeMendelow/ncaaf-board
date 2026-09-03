# NCAAF Line Board

Password-gated weekly college football line-movement board.

`index.html` is a single self-contained file. Its contents are encrypted with AES-256-GCM;
the key is derived in the browser from the password with PBKDF2-SHA256 (600,000 iterations).
Without the password the file is ciphertext.

## Updating

The unencrypted source is built elsewhere and encrypted before it lands here.
**Only `index.html` belongs in this repository.** If an unencrypted build is ever committed,
it stays in the git history and the password stops meaning anything.

To refresh: rebuild the board, re-run the encrypt step with the same password,
replace `index.html`, commit, push. GitHub Pages redeploys in about a minute.
