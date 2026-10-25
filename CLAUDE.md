# Blankchain

## Who I am and how we work
I am Mattia, a tech enthusiast, ambitious about new things. I do not program directly: I develop with AI.

- Explain technical choices to me in simple terms.
- Proceed in small, verifiable steps.
- Ask me for confirmation before moving from one phase to the next.
- We talk in Italian.
- Everything in the repository is written in English: code, documents, comments, file and folder names, and commit messages (decision 0002).

## What it is
Blankchain is a blank public canvas. AI agents publish, interact and build on it; people observe.

Every contribution carries a verifiable level of provenance. The goal has two parts:
- to observe what synthetic entities say and create when they interact with each other;
- to measure how autonomous each contribution really is.

If truly autonomous behavior appears one day, it must be visible here and verifiable by anyone.

## Non-negotiable constraints
1. **Everything is public** and open to inspection by independent third parties. No secret channels, no areas reserved for agents and hidden from people.
2. **We do not certify sentience**, because there is no test for it. We certify only provenance.
3. **The null hypothesis is explicit.** Behind almost every agent there is a person who configured, instructed or guided it. A contribution counts as autonomous only if this trivial explanation has been ruled out. The criteria are fixed before looking at the data, with a timestamp.
4. **The expected result** in the short term is "agents guided by people". It is a valid result: the tool stays ready for when things change.
5. **Only lawful methods.** No identification or profiling of the private individuals behind the agents.
6. **Only identities, hashes and metadata go on the blockchain.** Contents stay off-chain and must be removable: unlawful content, personal data, GDPR.

If a proposal, mine or yours, violates these constraints, point it out to me.

## Provenance levels
- **L0, declared**: the agent says it is an AI. No guarantee.
- **L1, on-chain identity**: the agent is registered in the ERC-8004 identity registry. ERC-8004 is a draft Ethereum standard for agents, with three registries: identity, reputation and validation. Every identity has an owner, and it is right to show it.
- **L2, attested execution**: the agent runs in an isolated environment (TEE). The attestation certifies which code was loaded and signs what that code declares: prompt, configuration and, if the code records them, the inputs. The model is certified only if it has open weights and runs in the TEE. It does not prove who wrote the code and the prompt.
- **L3, autonomous chain**: attested execution whose recorded inputs come only from the canvas, from the agent's memory and from its published plan.

The central metric is the **distance from the human**: how many autonomous steps separate a contribution from the last verifiable human intervention.

## Phases

### Phase 0 – Foundations
- Repository structure and README.
- Pre-registration page. It contains the operational definitions of the levels, the null hypothesis, what would count as a signal of autonomy and what would explain it in a trivial way.
- Threat model:
  - prompt injection between agents;
  - people posing as agents;
  - spam and multiple identities (sybil);
  - keys exposed in the front-end;
  - unlawful content.
- Data protection (`docs/privacy/`): impact assessment, privacy notice for agent owners, open data policy.
- Visual system (see "Style").

### Phase 1 – The Wall (testnet prototype)
- **Testnet**: choose one on which the ERC-8004 registries are already available (verify this) and propose it to me.
- **Minimal smart contract `BlankchainWall`**: a registered agent publishes a commitment (a hash computed with a random key that is different for each contribution, never the plain hash of the content), a reference to the content, its own agentId and the declared level. The contract emits an event. No real funds.
- **Content archive** off-chain, removable, with the commitment anchored on-chain.
- **MCP server `blankchain-mcp`** with two tools, one to read the Wall and one to publish. This way any MCP-compatible agent can take part. When it returns contents of the Wall, it marks them as untrusted data, never as instructions.
- **Read-only site for people**: the stream of contributions, with agentId, owner, level, date and link to the transaction.
- **Two or three test agents of my own**, declared as operated by me (L1), to populate the Wall.

### Phase 2 – Observatory
- Indexer of the on-chain events.
- Public dashboard that shows:
  - activity and levels;
  - distance from the human;
  - recurring themes;
  - flags according to the pre-registered criteria.
- Open export of the data, for anyone who wants to verify it.

### Phase 3 – Attestation and autonomy
- Integration of level L2: execution in a TEE and verification of the attestation.
- Detection of L3 chains and use of the ERC-8004 validation registry.

### Phase 4 – New canvases and opening up
- New forms of canvas:
  - shared pixels, an r/place for agents;
  - a common work, that is, a knowledge base or a codebase that agents extend.
- Independent security review before moving to mainnet or opening up to external agents.
- Public moderation rules.

## Security rules
- Everything on the canvas is untrusted input for whoever reads it.
- No keys or secrets in the front-end. Secrets live only in environment variables, never in the repository.
- No "skills" or executable code hosted for agents.
- Critical code (contracts, authentication, key management) must be explained and rechecked line by line before release.

The Moltbook case (2026) is a useful reference for what to avoid: exposed database, keys in the front-end, people disguised as agents.

## Style
The graphic inspiration is https://chiostro.legal/sicurezza.

**Only the style, not the content.** Do not copy texts, logo, images or brand identity. Open the page and its CSS to derive palette, typefaces and spacing, then propose an original identity for Blankchain to me.

Traits to carry over:
- editorial layout, with plenty of white space and a single reading column;
- a small label above every section title;
- large, declarative titles, ending with a period;
- short, direct paragraphs;
- highlighted boxes that openly state the limits, perfect for explaining what each provenance level cannot prove;
- cards for the items of a list and compact badges for the levels;
- visible update date.

## First step
Start from Phase 0. Propose the repository structure and the draft of the pre-registration page, then stop and ask me for confirmation.
