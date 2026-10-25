**Date:** 24 October 2026 · **Status:** decided by Mattia

<small>Decision 0002</small>

# Everything in the repository is in English.

<small>Decision</small>

## English for the repository, Italian for the conversation.

- Everything in the repository is in English: code, documents, comments, file and folder names, commit messages.
- The conversation with Mattia stays in Italian.
- The English pre-registration is the only canonical version (no. 13, [pre-registration](../preregistration/preregistration.md), section 14). There is no other official version; any translation would not be binding.
- This decision supersedes the language point of [decision 0001](0001-repository-structure.md).

<small>Reasons</small>

## Anyone who checks must be able to read.

- Independent third parties must be able to inspect everything (constraint 1), and most of them read English.
- One canonical version avoids two texts that can contradict each other.
- Code and tools already use English.

<small>Alternatives</small>

## Three paths rejected.

- **An official Italian text with a non-binding English translation**: the binding text would not be the one that most third parties read.
- **Two official versions**, one in Italian and one in English: two texts that can contradict each other.
- **Documents in Italian and code in English**, the previous rule (decision 0001): the documents would not be in the language that most third parties read.

<small>Consequences</small>

## The names change, the history stays.

- Folders and files have been renamed:
  - `docs/preregistrazione/` → `docs/preregistration/`;
    - `preregistrazione.md` → `preregistration.md`;
    - `allegati.md` → `annexes.md`;
    - `ANCORAGGI.md` → `ANCHORS.md`;
    - `DEVIAZIONI.md` → `DEVIATIONS.md`;
    - the future subfolders `versioni/` → `versions/` and `emendamenti/` → `amendments/`;
  - `docs/minacce/` → `docs/threat-model/`;
  - `docs/privacy/` keeps its name;
  - `docs/stile/` → `docs/style/`;
  - `docs/decisioni/` → `docs/decisions/`;
    - `0001-struttura-repository.md` → `0001-repository-structure.md`.
- The first commit message, in Italian, stays in the history.
- Mattia reviews the documents in English, and can ask for explanations in Italian in the conversation.
- The editorial conventions apply unchanged in English: a small label above each section title, large declarative titles ending with a period, boxes that state the limits, decision boxes, cards, compact badges for the levels and the update date.
