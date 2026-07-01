# Security Centre Platform
 
A production-grade backend system built to scan and assess security posture across cloud infrastructure — detecting malware, secrets, vulnerabilities, and generating comprehensive security reports.
 
## Scale & Impact
- Scans thousands of hosts, containers, and pods in real-time
- Generates 4,000-5,000 SBOM and reports
- Supports high-throughput, parallel scan processing
- Handles massive data ingestion without performance degradation
 
## Tech Stack
- **Backend**: (Golang, Apache Kafka) — high-performance server handling scanning and data processing
- **Database Architecture (Hybrid)**:
  - **Neo4j**: Graph database for relationship mapping between hosts, containers, pods, and vulnerabilities
  - **PostgreSQL**: Relational data storage for scanning results and metadata
  - **Redis**: In-memory caching for query optimization and session management
- **Storage**: MinIO - open-source, high-performance, S3-compatible object storage system.
 
## Problem I Solved
 
**Challenge & Solution**
 
Neo4j faced severe locking with 150+ million relationships. Community edition bulk ingestion limits created bottlenecks during continuous data ingestion.
 
Implemented hot/cold data strategy — last 2 scans in active database, 1-year historical data archived separately. This eliminated locking contention, improved query performance, and enabled real-time scanning without infrastructure upgrade.
 
## Key Features
- vulnerability detection
- Malware and secret scanning across infrastructure
- Security posture assessment and reporting
- Historical data analysis and trend tracking
 
