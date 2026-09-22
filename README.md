# GitHub Update Source Test

This repository content is a static update-source smoke test for ComPDF Self Hosted.

Updater base URL:

```text
https://raw.githubusercontent.com/C-WangPengHui/Self-hosted/main/compdf/
```

The updater appends the configured channel and reads:

```text
compdf/stable/release.json
compdf/stable/release.json.sig
compdf/stable/compose.release.yml
compdf/stable/checksums.txt
```

The Ed25519 public key used for this test is in `release-public-key.txt`.
The currently published acceptance manifest references the local test registry:

- `localhost:5000/compdf-app:5.0.0`
- `localhost:5000/compdf-server:5.0.0`

Images are pinned by the digests in `release.json`; this is a local acceptance
publication and is not a public Docker Hub image release.
