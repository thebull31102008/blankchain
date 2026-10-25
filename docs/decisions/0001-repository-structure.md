**Date:** 24 October 2026 · **Status:** approved by Mattia

<small>Decision 0001</small>

# One repository, with folders that are created phase by phase.

<small>Decision</small>

## One repository, folders by phase, separate licenses.

- A single repository, public as soon as we publish it, for documents, contracts, archive, MCP server, site, test agents and indexer.
- The public documents are in `docs/`: pre-registration, threat model, privacy, style, decisions.
- A folder is created only when its phase starts. Today the root, `LICENSES/` and `docs/` exist.
- The documents are in Italian. The code will use English names. **Superseded by [decision 0002](0002-english-only.md).**
- LF line endings and UTF-8 for all text files, set in `.gitattributes` and `.editorconfig`.
- Licenses: MIT for the code, CC BY 4.0 for the documents, CC0 1.0 for the exports of aggregate data.
- Data protection (`docs/privacy/`) becomes part of Phase 0.

<small>Reasons</small>

## Everything can be verified in a single history.

- A single repository lets third parties verify everything in a single version, with a single history.
- Empty folders give the impression of work that does not exist, and git does not keep them.
- The hash (a cryptographic fingerprint) of the pre-registration must be identical on every computer. On Windows, CRLF line endings would change it.
- MIT is designed for code and CC BY for texts. CC0 leaves the aggregate data reusable without copyright conditions.
- The research for the pre-registration showed that the owners' addresses can be personal data (EDPB Guidelines 02/2025, version 2.0). This must be assessed before the deployment.

<small>Alternatives</small>

## Three paths rejected.

- **Creating all the folders right away**, empty: rejected for the reasons above.
- **Separate repositories** for contracts, server and site: harder for third parties to verify.
- **A single license for everything**: none fits both code and texts.

<small>Consequences</small>

## Tools and publication remain to be chosen.

- The development tools remain to be chosen: Hardhat or Foundry, static site, package management, automatic check for secrets before every commit. Each one will have its own record in Phase 1, and every code folder will have its own `.gitignore` for generated files.
- Per-contribution exports and content exports will not be in `data/`: their license will be decided in the open data policy.
- The copyright holder in the `LICENSE` file is "The Blankchain authors". It can be replaced with a name.
- The repository is local only. Before publishing it on GitHub: turn on private vulnerability reporting, secret scanning with push protection and protection of the `main` branch; then update the link in `SECURITY.md`.
