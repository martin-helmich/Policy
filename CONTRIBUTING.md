# Contributing to the TYPO3 Association Policy Repository

This repository governs the TYPO3 Association's policies and bylaws, and the
changes made to them. All changes are tracked using Git and GitHub pull
requests.

This process is governed by a TYPO3 Association Board decision, documented in
[`Documentation/Association/Board/Decisions/2026/07-09-PolicyGovernance.rst`](Documentation/Association/Board/Decisions/2026/07-09-PolicyGovernance.rst).

## Ownership

Every policy document specifies an **owner** on the line just below its H1
title. The owner is who can authorize changes to that document — for example:

> This policy can only be changed through a decision by: TYPO3 Association
> General Assembly.

Decisions about ownership itself are made by the TYPO3 Association Board. The
TYPO3 Association General Assembly can be represented by members of the TYPO3
Association Board.

## Types of changes

Every pull request must be handled as **one, and only one,** of the following
change types. No files can be changed unless the pull request is classified
correctly. This classification is enforced automatically and is reflected in a
label on the pull request.

### Maintenance changes

Changes that **do not** change the meaning of the text — for example,
correcting a link that leads to a 404 page, or fixing a typo.

- Label: `type: maintenance change`
- Requires **1 approval** by a representative of the owner.
- The decision can be documented in the commit message; no separate decision
  document is required.

### Formal changes

Changes **to the meaning** of the text. These require a formal decision by the
owner, in accordance with the owner's decision-making rules.

- Label: `type: formal change`
- Requires **2 approvals** by representatives of the owner.
- Must include a **separate decision document** in the pull request,
  conforming to the owner's decision-documentation rules. For example, a TYPO3
  Association Board decision to change the Reimbursement Regulations is added as
  a new file under
  [`Documentation/Association/Board/Decisions/`](Documentation/Association/Board/Decisions/).

### Bylaw changes

Any change to the bylaws
([`Documentation/Association/BylawsAndProceedings.rst`](Documentation/Association/BylawsAndProceedings.rst))
is a special kind of formal change. Each change to the bylaws must be
substantiated by a two-thirds majority vote of the General Assembly.

- Label: `type: bylaw change` (applied automatically when the bylaws file is
  touched).
- Requires **2 approvals** by representatives of the owner.
- **Every commit** that touches the bylaws file must include a link to the
  relevant General Assembly protocol (a `https://typo3.org/...` URL) in its Git
  commit message. The protocol serves as proof of the required vote, and a pull
  request is only merged if such a protocol recorded the vote for the change.
- When approving, make sure the changes match those approved in the General
  Assembly protocol, and that the non-authoritative English translation of the
  bylaws is updated accordingly.

## Documenting decisions

All changes must be merged as pull requests that document the decision
authorizing the change:

- **Maintenance changes** — documented in the commit message.
- **Formal changes** — documented in a separate decision document included in
  the pull request.
- **Bylaw changes** — substantiated by a linked General Assembly protocol.

## How this is enforced

Because GitHub branch protection rules cannot express these requirements, they
are enforced through GitHub Actions workflows in
[`.github/workflows/`](.github/workflows/):

- **Check change type** — asserts that every pull request carries exactly one
  change-type label, automatically labels bylaw changes, and requires formal
  changes to add a new decision record under
  `Documentation/Association/Board/Decisions/`.
- **Check approvals** — asserts that the pull request has the number of
  approvals required by its change-type label (1 for maintenance, 2 for formal
  and bylaw changes).
- **Bylaw change** — asserts that every commit touching the bylaws links to the
  relevant General Assembly protocol.

Changing these workflows (apart from maintenance changes) requires a formal
Board decision, documented in the same manner.
