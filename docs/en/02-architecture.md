# Architecture

Acecore is designed as a federated architecture, not as a single centralized organization.

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

Acecore begins with areas that can be built outside the state, such as cooperation, education, welfare, trust, and infrastructure.

The initial repository only creates module directories for Identity, Economy, Welfare, Governance, Arbitration, and Infrastructure. Reputation and Audit are important design layers, but they can remain inside related modules until the need for independent modules becomes clear.

## Design Direction

Acecore separates functions into modules and connects them through open protocols. This keeps the system easier to improve, replace, audit, and fork.
