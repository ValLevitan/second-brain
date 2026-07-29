# Flex-POS Ecosystem Context

> **Purpose:** This file gives Claude (and developers) full cross-repository awareness of the Flex-POS platform. It is the single source of truth for how services relate, communicate, and deploy.
>
> **Maintenance:** Update this file whenever a service changes its API surface, communication patterns, or deployment topology. The owning team is responsible for keeping their section current.

---

## Repositories & Service Ownership

| Repository | Service Name | Domain | Owner | Purpose |
|---|---|---|---|---|
| `terminal-hub` | Terminal Hub | POS terminal management | _TBD_ | _One-line description_ |
| `customer-management` | Customer Management | Customer data & profiles | _TBD_ | _One-line description_ |
| `location-management` | Location Management | Store/site configuration | _TBD_ | _One-line description_ |
| `location-billing` | Location Billing | Billing per location | _TBD_ | _One-line description_ |
| `payment-hub` | Payment Hub | Payment processing | _TBD_ | _One-line description_ |
| `flex-pos-station` | Flex-POS Station | On-device POS application | _TBD_ | _One-line description_ |
| _infra repo(s)_ | — | Infrastructure / deploy | _TBD_ | _IaC, CI/CD, shared config_ |

---

## Inter-Service Communication

### Communication Map

```
┌─────────────────┐       REST/gRPC        ┌──────────────┐
│  Flex-POS        │ ───────────────────►   │ Terminal Hub  │
│  Station         │                        └──────┬───────┘
└─────────────────┘                                │
                                                   │ events
                                                   ▼
                                          ┌──────────────────┐
                                          │  Payment Hub      │
                                          └──────────────────┘
```

> **TODO:** Replace this placeholder with the actual communication topology.

### Protocols & Patterns

| From → To | Protocol | Pattern | Notes |
|---|---|---|---|
| Station → Terminal Hub | _REST / gRPC / WebSocket_ | _sync / async_ | _Auth mechanism, retry policy_ |
| Terminal Hub → Payment Hub | _event bus / REST_ | _pub-sub / request-reply_ | _Topic/queue names_ |
| _...add all pairs..._ | | | |

### Shared Contracts & Schemas

- **API specs:** _Where do OpenAPI / protobuf definitions live? Link to files or directories._
- **Event schemas:** _Where are event payloads defined? Schema registry?_
- **Shared types/models:** _Any shared library or package for common data structures?_

---

## Service Discovery & Runtime Topology

### Environments

| Environment | Purpose | Access |
|---|---|---|
| `dev` | Local / developer | _How to run locally_ |
| `staging` | Pre-production | _URL pattern or how to reach_ |
| `production` | Live | _URL pattern_ |

### How Services Find Each Other

_Describe the mechanism: DNS-based discovery, service mesh (Istio/Linkerd), environment variables, config maps, hardcoded URLs, etc._

```
# Example: environment variable pattern
TERMINAL_HUB_URL=https://terminal-hub.{env}.flexpos.internal
PAYMENT_HUB_URL=https://payment-hub.{env}.flexpos.internal
```

### Infrastructure Stack

- **Orchestration:** _Kubernetes / ECS / VMs / other_
- **Message broker:** _Kafka / RabbitMQ / SQS / other_
- **Database strategy:** _DB-per-service? Shared DB? Which engines?_
- **CI/CD:** _Where pipelines live, deploy order dependencies_

---

## Deployment Dependencies & Ordering

_Which services must be up before others? Are there migration ordering constraints?_

```
1. Infrastructure (networking, message broker, databases)
2. Location Management (foundational reference data)
3. Customer Management
4. Terminal Hub
5. Payment Hub (depends on Terminal Hub)
6. Location Billing (depends on Location Management)
7. Flex-POS Station (depends on Terminal Hub, Payment Hub)
```

> **TODO:** Validate this ordering with infra team.

---

## Cross-Repo Development Patterns

### When changing a service API:
1. Update the contract/schema in the owning repo
2. Update the **Inter-Service Communication** section in this file
3. Check downstream consumers in the communication map above
4. Coordinate breaking changes across repos before merging

### When adding a new service:
1. Add it to the **Repositories & Service Ownership** table
2. Add all communication pairs to the **Communication Map**
3. Add deployment ordering constraints
4. Update the bootstrap script

### Common pitfalls:
- _List known integration gotchas, e.g., "Payment Hub expects Location ID in header, not body"_
- _List any shared assumptions that aren't obvious from individual repos_

---

## Local Development Setup

### Prerequisites
_Runtime versions, tools, credentials needed._

### Bootstrap

```bash
# Clone all ecosystem repos into a standard layout
./bootstrap.sh

# Expected directory structure after bootstrap:
# flex-pos/
# ├── .claude/
# │   └── CLAUDE.md          ← this file (symlinked or copied)
# ├── terminal-hub/
# ├── customer-management/
# ├── location-management/
# ├── location-billing/
# ├── payment-hub/
# ├── flex-pos-station/
# └── infra/
```

### Running the full stack locally
_Docker compose? Tilt? Individual service startup commands?_

---

## Open Questions

_Track unresolved architectural or integration questions here. Move to individual repos once resolved._

- [ ] _Example: Should Station talk directly to Payment Hub or always through Terminal Hub?_
- [ ] _Example: Event schema versioning strategy — who owns the schema registry?_
