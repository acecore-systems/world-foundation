# Architecture

World Foundation Design uses a federated architecture, not a single centralized organization.

Its architecture separates social functions into modules and connects them through open protocols. This makes it easier to improve, replace, review, and fork parts of the system without forcing every participant into one implementation.

## Core Modules

- Identity
- Reputation
- Economy
- Welfare
- Governance
- Arbitration
- Infrastructure
- Audit

Each module should have a clear responsibility and should not accumulate excessive authority.

This design begins with areas that can be built outside the state, such as cooperation, education, welfare, trust, and infrastructure.

The initial repository only creates module directories for Identity, Economy, Welfare, Governance, Arbitration, and Infrastructure. Reputation and Audit are important design layers, but they can remain inside related modules until the need for independent modules becomes clear.

## Design Direction

This design separates functions into modules and connects them through open protocols. This keeps the system easier to improve, replace, audit, and fork.

## Relationship with State Functions

This design does not attempt to replace all state functions at once.

It begins with areas that can be explored through voluntary cooperation, such as documentation, shared knowledge, mutual aid, governance experiments, trust, welfare, education, and infrastructure.

Over time, useful cooperation infrastructure may reduce dependency on state boundaries and centralized institutions.
