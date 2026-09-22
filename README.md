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
The manifest references the Docker Hub images:

- `compdfkit/compdf-app:5.0.0`
- `compdfkit/compdf-server:5.0.0`

Images are pinned by the digests in `release.json`; the release metadata is
still a smoke-test publication, not a claim that the images are public to every
Docker Hub account.
