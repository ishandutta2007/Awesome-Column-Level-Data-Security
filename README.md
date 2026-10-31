# Awesome-Column-Level-Data-Security

# Awesome-Column-Level-Data-Security

**Top Column Level Data Security (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Dynamic Masking, Tokenization, Attribute-Based Access Control & Self-Hosted Data Security*

**Last updated: November 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Column-Level Data Security**. These tools enable organizations to protect sensitive fields—PII, financial records, health data—by masking, tokenizing, or encrypting specific columns while preserving data utility for authorized users—from fully managed platforms with centralized policy engines and discovery to self-hosted gateways and libraries that give teams complete control over their data protection layer.



**Examples** include Snowflake Column-Level Security, Immuta, Privacera, Satori, Cyral, Protegrity, Baffle, ALTR, Varonis, and SecuPi (the category leaders in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosted column security, dynamic masking, and open policy enforcement. **Critical note**: The open-source column-level security landscape is fragmented—**Apache Ranger** is the most mature policy engine for Hadoop ecosystem masking , **dsacp** extends Ranger to ClickHouse/Doris/StarRocks with a proxy , and **Greenmask** handles static anonymization for PostgreSQL dumps . No single open-source project matches Immuta's centralized ABAC across multiple data platforms or Privacera's format-preserving encryption at scale, but for specific ecosystems, the open-source options are production-proven.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## Sector Overview & Market Dynamics

The global data security and data access governance (DAG) sector is estimated at **$14.7B – $17.2B in 2025–2026** (scaling past $37B by 2031 at ~17% CAGR), with dedicated data access governance accounting for ~$2.1B+ and rapidly rising. The market is **moderately fragmented** rather than winner-take-all: high-scale cloud platforms (Snowflake, Databricks, Hyperscalers) capture baseline storage governance, while specialized pure-play platforms compete intensely and drive active M&A activity for cross-platform attribute-based access control (ABAC), tokenization, and dynamic runtime masking.

## SaaS/Hosted Platforms

| Platform | Company Size (Valuation / Revenue) | Pricing | Free Tier / Trial Limit | Key Capabilities & Best For |
| :--- | :--- | :--- | :--- | :--- |
| **[Snowflake Column-Level Security](https://www.snowflake.com/)** | **~$110B–$115B** Market Cap / ~$5.9B Revenue | Dynamic Data Masking requires Enterprise Edition starting at **$3.00/credit** (Standard is $2.00/credit, Business Critical is $4.00/credit; on-demand) | **30-day free trial** with **$400 in usage credits** (trial ends after 30 days or when $400 is depleted; no forever-free tier) | Native masking policies and external tokenization within Snowflake; best for Snowflake-centric workloads without 3rd-party tools. |
| **[Commvault / Satori](https://www.satori.ai/)** | **~$7.0B–$7.4B** Market Cap / ~$1.22B Revenue *(Commvault acquired Satori; standalone was $95k/yr avg)* | Enterprise contract starting around **$95,000/year** (Satori standalone average deal via Commvault data security offerings) | **Vendor-guided trial / interactive sandbox** (no self-serve forever-free tier) | Universal Data Access Service providing dynamic masking, access workflows, and discovery across multi-cloud stores. |
| **[Varonis](https://www.varonis.com/)** | **~$5.6B** Market Cap / ~$688M Revenue | Starting around **$55 – $95/user/year** (base Microsoft 365 coverage) to **$80 – $140/user/year** (multi-platform DSPM/coverage); typical enterprise minimums ~$15k–$50k/yr | **30-day free trial** (enterprise evaluation/guided data risk assessment; no forever-free tier) | Data security platform with column-level discovery, classification, and permissions right-sizing. |
| **[Immuta](https://www.immuta.com/)** | **~$1.0B** Valuation (Series E Unicorn) / ~$23M+ ARR | Annual contract pricing starting at **$96,000/year** (baseline AWS Marketplace 12-month tier covering 960 Immuta Units) | **14-day free trial** (available via AWS Marketplace / guided sandbox; no forever-free tier) | Dynamic attribute-based access control (ABAC) natively translated into Snowflake, Databricks, Redshift, and Starburst. |
| **[Privacera](https://www.privacera.com/)** | **~$250M–$500M** Est. Valuation / ~$38.5M Revenue | Foundation package starting at **$100,000/year** (12-month Data Access Governance Starter Pack on AWS Marketplace) | **30-day free trial** on cloud environments (PrivaceraCloud evaluation; no forever-free tier) | Policy-driven encryption and masking via PEG (Privacera Encryption Gateway); format-preserving encryption (FPE) and tokenization. |
| **[ALTR](https://www.altr.com/)** | **~$100M–$250M** Est. Valuation / ~$8M–$10M Revenue | Paid tier starts at **$10/data user/month** (Enterprise plan; custom quotes for enterprise scale) | **Free Forever Tier**: **$0/month** (up to 3 connected databases, full data classification, and dynamic masking via Snowflake Partner Connect) | Tag-based dynamic column masking and data governance with native Snowflake & cloud warehouse integration. |
| **[Baffle](https://baffle.io/)** | **~$100M–$250M** Est. Valuation / ~$3.3M ARR | Instance-based metered pricing from **~$0.40 – $1.50/hour** (depending on EC2 instance size e.g. t3.large to m5.xlarge; enterprise contracts via private offer) | **30-day free trial** (available on AWS Marketplace for RDS, Aurora, and S3; excludes underlying AWS infra costs) | No-code cryptographic protection; field- and column-level format-preserving encryption without application code changes. |
| **[Protegrity](https://www.protegrity.com/)** | **~$50.7M** Est. Revenue (~$25M–$100M industry range) | Enterprise contract-based units; minimum annual deployments typically start at **~$50,000 – $100,000/year** via AWS private offers | **30-day free trial** on select modules (e.g., Cloud Protect for S3; enterprise PoC on request; no forever-free tier) | Enterprise-grade tokenization and format-preserving encryption using warehouse User-Defined Functions (UDFs). |
| **[Cyral](https://cyral.com/)** | *Acquired by Varonis ($5.6B Market Cap)* | Base plans start at **$50/month** (scales to ~$500/database/month for advanced monitoring and fine-grained controls) | **Free Forever Plan**: limited to **1 single user and basic discovery on 1 database**; plus a 14-day full feature trial | Database security and activity monitoring proxy enforcing column-level access controls and granular query policies. |
| **[SecuPi](https://secupi.com/)** | Bootstrapped / Est. **~$3.4M–$8.4M** Revenue | Enterprise annual subscriptions; minimum 12-month commitments typically starting at **~$30,000 – $60,000/year** based on protected data sources | **30-day free trial** (available for Policy Administration Server on AWS Marketplace; no forever-free tier) | Proactive dynamic authorization, de-identification (FPE, tokenization, masking), and real-time column-level policy enforcement. |

## Open-Source GitHub Projects



- **[Apache Ranger](https://github.com/apache/ranger)**

  **Framework for centralized security policy administration** (Apache 2.0) — **the most mature open-source policy engine for column-level masking** in the Hadoop ecosystem. **Features**: **Column masking policies** for Hive and Spark SQL—define which users see masked values for specific columns ; **Row-level filtering**; **Centralized audit** of all access attempts; **Policy management UI**; integrates with Hive, Spark, Kafka, HDFS, and more; **IBM watsonx.data** uses Ranger for column masking . **Tech stack**: Java. **Deploy**: Self-hosted (requires Hadoop ecosystem or compatible platform). **Trade-off**: **Hadoop-ecosystem-centric**—native support limited to Hive, Spark, Kafka, HDFS. **No native support for modern OLAP databases** (ClickHouse, Doris, StarRocks) without additional integration. **Best for**: organizations running Hadoop/Spark ecosystems wanting centralized column masking with audit—the foundation for open-source policy-driven security.



- **[dsacp (Unified Data Security Access Control Platform)](https://github.com/turtacn/dsacp)**

  **Open-source data security and access control platform extending Apache Ranger** (license per repo) — **the most practical open-source solution for column-level security in modern OLAP databases** . **Features**: **dsacp-proxy** (Golang) acts as a mandatory access point for **ClickHouse, Doris, StarRocks**—databases that lack native Ranger plugins; parses queries, fetches Ranger policies, enforces **dynamic data masking** on sensitive columns, and logs all access to Ranger Audit Store . **Unified policy management** via Apache Ranger Admin; **fine-grained authorization** at database, table, and column level; **high-performance proxy** with caching; **relatively transparent to business**—applications only need connection string changes. **Tech stack**: Golang (proxy), Apache Ranger (policy engine). **Deploy**: Self-hosted (Ranger + dsacp-proxy). **Trade-off**: **Proxy adds latency and operational complexity**; newer project with limited community validation. **Ranger itself is Hadoop-era**—UI and configuration may feel dated. **Best for**: organizations running ClickHouse, Doris, or StarRocks that need column-level masking and centralized policy management—especially those already using Ranger or willing to adopt it.



- **[Greenmask](https://github.com/GreenmaskIO/greenmask)**

  **Open-source logical database dump, anonymization, and restoration utility** (Apache 2.0) — **the most mature open-source tool for static column anonymization** in PostgreSQL. **Features**: **Database subsetting**—create smaller, referentially intact development databases; **deterministic transformation**—reproducible masking using hash functions; **dynamic parameters**—transformers adapt based on other column values; **transformation conditions**—apply transformations only when criteria are met; **storage-agnostic** (local, S3, MinIO, GCS, Azure); **dumps compatible with pg_restore** . **Tech stack**: Go. **Deploy**: Self-hosted (single binary). **Trade-off**: **Static masking only**—it anonymizes data in dumps, not at query runtime. **PostgreSQL-focused** (MySQL in progress). **Not a live access control system**—data is masked before it leaves the source. **Best for**: teams needing to create safe, anonymized copies of production PostgreSQL databases for development, testing, or analytics—the standard open-source tool for static data sanitization.



- **[SupaForge](https://github.com/musasen/supaforge)**

  **Zero-Trust Row-Level Security (RLS) & Column-Level Security (CLS) Engine for Supabase & PostgreSQL** (MIT, v0.2.0) — **the most developer-friendly open-source tool for declarative column-level privileges** in PostgreSQL. **Features**: **Fluent TypeScript DSL** compiles security rules into hardened PostgreSQL DDL/DCL policies; **fine-grained column-level security**—control read (r), create (c), and update (u) permissions down to individual columns; **multi-role inheritance** with diamond hierarchy resolution; **default-deny architecture**; **sequence exhaustion protection**; **dynamic policy lifecycle management**—purges obsolete policies during compilation . **Tech stack**: TypeScript, Drizzle ORM, PostgreSQL. **Deploy**: `npm install supa-forge postgres`. **Trade-off**: **Supabase/PostgreSQL-specific**—not for multi-platform column security. **Column privileges in PostgreSQL are coarse**—they grant SELECT/INSERT/UPDATE, not dynamic masking based on role attributes. **Best for**: Supabase developers wanting type-safe, declarative column-level access control in PostgreSQL—especially those who prefer code-defined policies over database-side policy engines.



### Additional Strong Open-Source Options



- **FloorVault** — Python library for field encryption with context binding (PyPI, Beta). AES-256-SIV encryption binds each field to its table/record/column coordinates—ciphertext moved to wrong context fails decryption . **Note**: **Application-level encryption**, not dynamic masking or access control—it protects data at rest, not query results. **Best for**: Python developers wanting to encrypt specific fields with context integrity.

- **PrivacyForge** — Local-first data de-identification platform (license per repo, MVP). Multi-layer PII detection (regex, NLP, dataset-aware, contextual), policy-driven transforms (redact, mask, tokenize, synthetic), verification with residual-PII rescan . **Note**: **Batch de-identification**, not runtime column security—it processes datasets, not live queries. **Best for**: teams needing to create anonymized datasets for sharing or development.

- **python-authz** — ReBAC/RBAC/ABAC authorization engine (PyPI, v0.5). Zanzibar-style relationship graph with SQLite/PostgreSQL backends . **Note**: **Authorization engine, not data masking**—it decides who can access resources, not how data is returned. **Best for**: developers building custom authorization with fine-grained permissions.



**Frameworks for building custom systems**: Combine **Apache Ranger** as the policy engine for Hadoop/Spark with **dsacp** to extend Ranger to ClickHouse/Doris/StarRocks, **Greenmask** for static anonymization of PostgreSQL dumps, and **SupaForge** for declarative PostgreSQL column privileges—creating a column security stack. **None of these match Immuta's cross-platform ABAC or Privacera's format-preserving encryption at scale**, but for specific ecosystems, the open-source options cover core needs.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Column-level data security platforms handling PII and regulated data must comply with data protection regulations (GDPR, HIPAA, PCI DSS, CCPA, etc.) and implement appropriate encryption, access controls, and audit logging.

- **The "dynamic masking" vs. "static anonymization" vs. "encryption" vs. "column privileges" distinction is critical.** **Snowflake, Immuta, Privacera, ALTR, Baffle, and SecuPi** provide **dynamic masking**—data is masked at query runtime based on user context . **Greenmask and PrivacyForge** are **static anonymization**—data is transformed before it leaves the source . **FloorVault** is **application-level encryption**—it encrypts fields at rest, not query results . **SupaForge** and PostgreSQL column privileges are **access control**—they grant or deny column access, but do not mask values dynamically . **Apache Ranger** provides **dynamic masking** for Hadoop ecosystems . **Choose based on whether you need runtime masking, batch anonymization, encryption, or access control.**

- **Apache Ranger is the most mature open-source policy engine for column masking** in Hadoop ecosystems—used by IBM watsonx.data and available for Hive/Spark/Kafka . **The trade-off**: Hadoop-era architecture; no native support for modern OLAP databases.

- **dsacp fills the gap for ClickHouse, Doris, and StarRocks**—it proxies queries through Ranger policy enforcement, enabling column masking in databases that lack native Ranger plugins . **The trade-off**: proxy adds latency; newer project with limited validation. **For teams running these OLAP engines and already using Ranger, it is the most practical open-source path.**

- **Greenmask is the standard open-source tool for static PostgreSQL anonymization**—deterministic masking, database subsetting, and pg_restore compatibility . **The trade-off**: static only—not runtime masking. **Use it to create safe development/test databases, not to protect live production queries.**

- **SupaForge is the most developer-friendly PostgreSQL column privilege tool**—declarative TypeScript DSL, default-deny, and policy lifecycle management . **The trade-off**: PostgreSQL column privileges are coarse (SELECT/INSERT/UPDATE grants), not dynamic masking. **For Supabase developers wanting code-defined column access control, it is the best option.**

- **Satori is no longer independent**—it was acquired and is now part of Commvault . **Do not evaluate Satori as a standalone option**; evaluate Commvault's integrated offering instead.

- **Pricing opacity is universal across commercial vendors.** Snowflake publishes credit-based pricing. Immuta, Privacera, Protegrity, Baffle, ALTR, Varonis, and SecuPi require sales contact. **Validate with direct vendor conversations against your data volume and platform count.**

- Self-hosted open-source solutions require proper infrastructure (Ranger for dsacp, Go runtime for Greenmask), security hardening for proxy credentials, and ongoing maintenance. **Column security tools have privileged access to sensitive data**—ensure your deployment meets your organization's compliance requirements before connecting production databases.



---



**Made for data security engineers, privacy officers, and organizations building transparent column-level data protection solutions.**

Let's make Column-Level Data Security more open, data-driven, and privacy-preserving.
