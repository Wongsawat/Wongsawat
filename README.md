# Hi there, I'm Weerachat Wongsawat 👋

## About Me

**Solution Architect & Senior Software Engineer** based in Bangkok, Thailand, specializing in enterprise integration and government-compliant document processing systems. I design and build high-reliability microservices platforms for Thailand's electronic tax invoice ecosystem.

## Tech Stack

| Area | Technologies |
|------|-------------|
| **Languages** | Java 17/21, Python |
| **Frameworks** | Spring Boot, Spring Cloud, Apache Camel |
| **Messaging** | Apache Kafka, Apache ActiveMQ |
| **Databases** | PostgreSQL, MongoDB |
| **Integration** | ebXML/ebMS 2.0, REST APIs |
| **Digital Signatures** | XAdES, PAdES, CSC API v2.0 |
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

Connect with me on [LinkedIn](https://www.linkedin.com/in/weerachat-wongsawat/) if you're working on e-government integration, digital signature implementations, telecom service delivery platforms, or ISO 20022 payment systems.
