# Hi there, I'm Weerachat Wongsawat

## About Me

**Solution Architect & Senior Software Engineer** based in Bangkok, Thailand, specializing in enterprise integration. I design and build enterprise integration platforms for Telecom, Banking and Government sectors — microservices, digital signatures, Open Banking payment initiation, and regulatory document processing.

## Tech Stack

| Area | Technologies |
|------|-------------|
| **Languages** | Java 17/21, Python |
| **Frameworks** | Spring Boot, Spring Cloud, Apache Camel |
| **Messaging** | Apache Kafka |
| **Databases** | PostgreSQL, MongoDB |
| **Integration** | ebXML/ebMS 2.0, REST APIs, Open Banking RW API v4.0.1 |
| **Digital Signatures** | XAdES, PAdES, CSC API v2.0 |
| **Payment Standards** | ISO 20022, FPS (pacs.008/pacs.002), BC-FIPS |
| **DevOps** | Docker, Kubernetes |

## Featured Projects

### [Thailand e-Tax Invoice Platform](https://github.com/Thailand-eTax-Project)

A production-grade microservices platform for processing, digitally signing, and submitting Thai e-Tax documents (Tax Invoice, Invoice, Receipt, Debit/Credit Notes, Cancellation Notes) to Thailand's Revenue Department via ebXML.

- **Saga orchestrator** coordinating distributed transactions across 22 microservices
- **Transactional outbox** with Debezium CDC for reliable event delivery
- **XAdES/PAdES digital signatures** via CSC API v2.0
- **PDF/A-3 generation** with embedded XML for archival compliance
- Supports 7 Thai e-Tax document types

#### Repositories (22 repos)

**Core Libraries**
| Repository | Description |
|-----------|-------------|
| [teda](https://github.com/Thailand-eTax-Project/teda) | Thai e-Tax Invoice JAXB library with database-backed code lists |
| [saga-commons](https://github.com/Thailand-eTax-Project/saga-commons) | Shared saga orchestration library |
| [eidasremotesigning](https://github.com/Thailand-eTax-Project/eidasremotesigning) | Remote Signing Service via CSC API v2.0 |

**Document Intake**
| Repository | Description |
|-----------|-------------|
| [document-intake-service](https://github.com/Thailand-eTax-Project/document-intake-service) | Document intake & validation |

**Processing Services (6)**
| Repository | Description |
|-----------|-------------|
| [invoice-processing-service](https://github.com/Thailand-eTax-Project/invoice-processing-service) | Invoice processing |
| [taxinvoice-processing-service](https://github.com/Thailand-eTax-Project/taxinvoice-processing-service) | Tax Invoice processing |
| [receipt-processing-service](https://github.com/Thailand-eTax-Project/receipt-processing-service) | Receipt processing |
| [cancellationnote-processing-service](https://github.com/Thailand-eTax-Project/cancellationnote-processing-service) | Cancellation Note processing |
| [debitcreditnote-processing-service](https://github.com/Thailand-eTax-Project/debitcreditnote-processing-service) | Debit/Credit Note processing |
| [abbreviatedtaxinvoice-processing-service](https://github.com/Thailand-eTax-Project/abbreviatedtaxinvoice-processing-service) | Abbreviated Tax Invoice processing |

**Signing Services**
| Repository | Description |
|-----------|-------------|
| [xml-signing-service](https://github.com/Thailand-eTax-Project/xml-signing-service) | XML digital signatures (XAdES) |
| [pdf-signing-service](https://github.com/Thailand-eTax-Project/pdf-signing-service) | PDF digital signatures (PAdES) |

**PDF Services (6)**
| Repository | Description |
|-----------|-------------|
| [invoice-pdf-generation-service](https://github.com/Thailand-eTax-Project/invoice-pdf-generation-service) | Invoice PDF/A-3 generation |
| [taxinvoice-pdf-generation-service](https://github.com/Thailand-eTax-Project/taxinvoice-pdf-generation-service) | Tax Invoice PDF/A-3 generation |
| [receipt-pdf-generation-service](https://github.com/Thailand-eTax-Project/receipt-pdf-generation-service) | Receipt PDF/A-3 generation |
| [cancellationnote-pdf-generation-service](https://github.com/Thailand-eTax-Project/cancellationnote-pdf-generation-service) | Cancellation Note PDF/A-3 generation |
| [debitcreditnote-pdf-generation-service](https://github.com/Thailand-eTax-Project/debitcreditnote-pdf-generation-service) | Debit/Credit Note PDF/A-3 generation |
| [abbreviatedtaxinvoice-pdf-generation-service](https://github.com/Thailand-eTax-Project/abbreviatedtaxinvoice-pdf-generation-service) | Abbreviated Tax Invoice PDF/A-3 |

**Storage & Downstream**
| Repository | Description |
|-----------|-------------|
| [document-storage-service](https://github.com/Thailand-eTax-Project/document-storage-service) | Document archive (MongoDB/S3) |
| [notification-service](https://github.com/Thailand-eTax-Project/notification-service) | Email/webhook notifications |
| [ebms-sending-service](https://github.com/Thailand-eTax-Project/ebms-sending-service) | ebXML submission to Revenue Dept |
| [orchestrator-service](https://github.com/Thailand-eTax-Project/orchestrator-service) | Saga orchestration coordinator |

---

### [PISP Open Banking Platform](https://github.com/wongsawat-pisp-openbanking)

A production-grade microservices platform implementing the UK Open Banking Read/Write API v4.0.1 specification for Payment Initiation Service Provider (PISP) flows. 18 microservices in a flat multi-module Maven monorepo covering domestic, international, scheduled, and standing-order payment workflows with full consent management.

- **Hexagonal architecture** (ports + adapters) across all services with domain/application/adapter/infrastructure layers
- **ISO 20022 payment rails** via Prowide-based FPS adapter (pacs.008 outbound, pacs.002 inbound) with end-to-end instruction traceability
- **Saga orchestration** with Kafka outbox pattern for reliable domain-event delivery (`pisp.domain-events`, `pisp.saga-commands`)
- **Security filter chain:** RawBodyCaching, BearerToken, MutualTLS, Idempotency, JWS verification, GrantType enforcement, ResponseSigning
- **BC-FIPS ready:** Optional `bcfips-integration` Maven profile activates Bouncy Castle FIPS PS256 signing
- **Comprehensive test strategy:** Domain unit tests, application slice tests, `@DataJpaTest` persistence, `@SpringBootTest` REST, and RestAssured + Testcontainers E2E

#### Service Groups (18 services)

**Payment Initiation**
| Service | Description |
|---------|-------------|
| domestic-payments | Domestic payment initiation with FPS rail adapter |
| international-payments | International payment initiation |
| file-payments | File-based bulk payment initiation |

**Scheduled Payments**
| Service | Description |
|---------|-------------|
| domestic-scheduled-payments | Future-dated domestic payments |
| international-scheduled-payments | Future-dated international payments |

**Standing Orders**
| Service | Description |
|---------|-------------|
| domestic-standing-orders | Recurring domestic payments |
| international-standing-orders | Recurring international payments |

**Consent Management**
| Service | Description |
|---------|-------------|
| domestic-payment-consents | Domestic payment consent authorisation |
| international-payment-consents | International payment consent authorisation |
| file-payment-consents | File payment consent authorisation |
| domestic-scheduled-payment-consents | Domestic scheduled payment consent authorisation |
| international-scheduled-payment-consents | International scheduled payment consent authorisation |
| domestic-standing-order-consents | Domestic standing order consent authorisation |
| international-standing-order-consents | International standing order consent authorisation |

**Infrastructure & Fee Engine**
| Service | Description |
|---------|-------------|
| saga-orchestrator | Distributed saga coordination |
| event-notification | Cross-cutting event notification |
| fee-engine | Fee calculation engine |
| fee-engine-demo | Fee engine demo frontend |
| fee-engine-admin-ui | Fee engine admin UI |
| fee-engine-ai-assistant | AI-powered fee engine assistant |

---

### [Thai Digital Academic Transcript Platform](https://github.com/Thailand-digital-transcript)

A microservices platform implementing the ETDA (Thailand) Digital Academic Transcript standard — ingesting transcript XML, validating against schema + Schematron business rules, driving multi-party approval + signing sagas (registrar → dean → university seal), and rendering PDF/A-3b documents with the sealed XML embedded.

- **Saga orchestration** with a transactional outbox (Camel-relayed `outbox_event` → Kafka)
- **XAdES/PAdES digital signatures** via CSC API v2.0 (eidasremotesigning)
- **PDF/A-3b generation** with embedded sealed XML, conformance gated by veraPDF
- **Hexagonal architecture** across all services (Java 17/21, Spring Boot)
- **Crash-safe signing** with explicit transaction boundaries (TX1 / TX1.5 / TX2) and idempotent replay

#### Repositories (7 repos)

| Repository | Description |
|-----------|-------------|
| [transcript-lib](https://github.com/Thailand-digital-transcript/transcript-lib) | JAXB bindings + Schematron + codelist JPA |
| [transcript-saga-commons](https://github.com/Thailand-digital-transcript/transcript-saga-commons) | Shared saga + transactional-outbox library |
| [transcript-processing](https://github.com/Thailand-digital-transcript/transcript-processing) | REST intake & source-XML ingestion |
| [transcript-orchestrator](https://github.com/Thailand-digital-transcript/transcript-orchestrator) | Saga orchestrator (batches) |
| [transcript-signing](https://github.com/Thailand-digital-transcript/transcript-signing) | XAdES (XML) + PAdES (PDF) signing |
| [transcript-pdf-generation](https://github.com/Thailand-digital-transcript/transcript-pdf-generation) | Sealed XML → PDF/A-3b |
| [e2e-harness](https://github.com/Thailand-digital-transcript/e2e-harness) | Cross-service E2E + compose topology |

---

Connect with me on [LinkedIn](https://www.linkedin.com/in/weerachat-wongsawat/) if you're working on e-government integration, digital signature implementations, telecom service delivery platforms, Open Banking payment initiation, or ISO 20022 payment systems.
