# Hi there, I'm Weerachat Wongsawat 👋

## About Me

Senior Software Engineer based in Bangkok, Thailand, specializing in enterprise integration and government-compliant document processing systems. I build high-reliability microservices platforms for Thailand's electronic tax invoice ecosystem.

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

- **19 Spring Boot microservices** orchestrated via saga pattern
- **Transactional outbox** with Debezium CDC for reliable event delivery
- **XAdES/PAdES digital signatures** via CSC API v2.0
- **PDF/A-3 generation** with embedded XML for archival compliance
- Supports 7 Thai e-Tax document types

#### Components

| Component | Description |
|-----------|-------------|
| [teda](https://github.com/Thailand-eTax-Project/teda) | Thai e-Tax Invoice JAXB library with database-backed code lists |
| [eidasremotesigning](https://github.com/Thailand-eTax-Project/eidasremotesigning) | Remote Signing Service via CSC API v2.0 |
| [invoice-microservices](https://github.com/Thailand-eTax-Project/invoice-microservices) | 16 Spring Boot services for document processing pipeline |

## GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=Wongsawat&theme=default&show_border=true)

![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=Wongsawat&layout=compact)

---

Feel free to reach out if you're working on e-government integration, digital signature implementations, or enterprise document processing systems.
