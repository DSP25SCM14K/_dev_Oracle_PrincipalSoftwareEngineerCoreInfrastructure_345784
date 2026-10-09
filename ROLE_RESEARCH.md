# Oracle Core Infrastructure Role Research

## Evidence and scope

The resume did not contain a job-description link. Search did not surface the exact requisition **345784**, so this assessment uses Oracle's closely matching Principal Software Engineer, Core Infrastructure posting (requisition 345544) and an earlier Core Infrastructure posting (344713) as adjacent evidence. The exact requisition should be checked if a direct link becomes available.

## Company and role context

Oracle Cloud Infrastructure builds and operates services across regions, availability domains, and fault domains. Oracle describes availability domains as isolated and fault tolerant, and explains that data-plane functions are designed to continue operating even when they are isolated from the corresponding regional control plane.

The closely matching Core Infrastructure role focuses on leading hyperscale distributed systems and data-plane services; designing for scalability, durability, availability, in-service updates, automatic failover, and recovery; optimizing data retrieval, storage, and processing; conducting performance and fault testing; and improving operational automation, security, and production response.

## Resume alignment

The portfolio centers the strongest evidence from the resume:

- Multi-tenant Java and Go OCI data-plane services with 99.99% availability across a 12K+ node fleet.
- High-throughput storage and processing paths with quorum replication and synchronized distributed state, sustaining p99 retrieval latency under 40 ms while tripling throughput.
- High-throughput Kafka data paths with 2B+ events per day, idempotent writes, replication, and durability guarantees.
- Fault-injection and brownout testing, SLOs, telemetry, alerting, incident response, Terraform automation, safe updates, and rollbacks.
- Java, Go, C++, cloud, Kubernetes, distributed storage, and production operations experience.

## Technical discussion areas

1. Explain invariants for a replicated metadata or storage service: leader changes, write acknowledgement, idempotency, data loss boundaries, and recovery.
2. Walk through overload behavior: admission control, load shedding, retries, backoff, timeouts, partition handling, and signals that drive each action.
3. Define availability and durability objectives, then relate metrics and fault tests to the objectives.
4. Describe safe production change: rollout gates, observability, rollback triggers, compatibility, and operator response.
5. Compare physical fault isolation in OCI across regions, availability domains, and fault domains with an application-level replication strategy.

## Sources

- [Oracle Careers: Principal Software Engineer, Core Infrastructure — 345544](https://careers.oracle.com/en/sites/jobsearch/job/345544/)
- [Oracle Careers: Principal Software Engineer, Core Infrastructure — 344713](https://careers.oracle.com/en/sites/jobsearch/job/344713)
- [OCI resilience and continuous availability FAQ](https://www.oracle.com/cloud/iaas/faq.html)
- [OCI regions and availability domains](https://docs.oracle.com/en-us/iaas/Content/General/Concepts/regions.htm)
