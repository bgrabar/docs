---
title: CockroachCloud Security
summary: Learn about the authentication, encryption, authorization, and audit log features for CockroachCloud clusters.
toc: true
redirect_from:
- ../stable/cockroachcloud-security-overview.html
---

A CockroachCloud cluster is single-tenant (no shared machines) running in a Virtual Private Cloud (no shared network) and has data encryption-in-flight enabled by default. Additionally, CockroachCloud provides authentication, authorization, and SQL audit logging features to secure your clusters.

The following table summarizes the CockroachCloud security features and provides links to detailed documentation for each feature where applicable.

Security feature | Description
-------------|------------
[Authentication](authentication.html) | <ul><li>Inter-node and node identity authentication using TLS 1.2</li><li>Client identity authentication using TLS 1.2 or username/password</li></ul>
Encryption | <ul><li>Encryption in flight using TLS 1.2</li><li>The backups for AWS clusters are encrypted using [AWS S3’s server-side encryption](https://docs.aws.amazon.com/AmazonS3/latest/dev/UsingServerSideEncryption.html) and the backups for GCP clusters are encrypted using [Google-managed server-side encryption keys](https://cloud.google.com/storage/docs/encryption/default-keys) </li></ul>
[User Authorization](user-authorization.html) | <ul><li>Users and privileges</li><li> Role-based access control</li></ul>
[Network Authorization](network-authorization.html) | <ul><li>IP allowlisting</li><li> VPC Peering for GCP clusters</li></ul>
[Audit logging](sql-audit-logging.html) | `ALTER TABLE...EXPERIMENTAL AUDIT` to get detailed information about queries being executed against your system
