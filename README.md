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
The manifest intentionally references the local test registry (`localhost:5000`);
this is not a production image publication.
