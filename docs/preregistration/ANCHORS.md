Updated 25 October 2026

<small>Pre-registration · Anchors</small>

# No version is anchored yet.

This is the version log cited in the [pre-registration](preregistration.md) (section 14) and in its [annexes](annexes.md). For each version anchored here, we record the SHA-256 hash (a cryptographic fingerprint) of each file and, for each file, the proofs of its date:

- the Bitcoin block of the OpenTimestamps proof;
- the RFC 3161 timestamps, alongside the public certificate of the authority that issued them, so that they can be verified even when that certificate is replaced;
- the signed tag and the immutable release on GitHub;
- if there are any, the DOI and the transaction on the testnet.

The frozen copies will go in `docs/preregistration/versions/`, the amendments in `docs/preregistration/amendments/`.

<small>Rule</small>

## The hash is computed on the bytes that git stores.

It is not computed on the copy of the file on your own computer, which an editor may have saved with different line endings. The file is in UTF-8 without BOM, with LF line endings. The command, at the commit that introduces the version:

```bash
git show <commit>:docs/preregistration/versions/v1.0/preregistration.md | sha256sum
```

It must be run in Git Bash, on Linux or on macOS. In Windows PowerShell 5.1, the symbols `|` and `>` re-encode the text and change the hash. The file timestamped with OpenTimestamps and RFC 3161 is the same one, extracted with `git cat-file blob <commit>:<path>`.

| Version | Date | File | SHA-256 | Proofs |
|---|---|---|---|---|
| none | | | | |
