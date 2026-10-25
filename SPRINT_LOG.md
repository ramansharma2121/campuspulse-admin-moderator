# 🗓️ CampusPulse (Admin & Moderator) — 12-Week Sprint Log

| Week & Dates | Strategic Focus | Deliverables & Work Completed | Obstacles & Mitigations | Status |
| :--- | :--- | :--- | :--- | :---: |
| **W1 (07/06 – 07/12)** | Department Schema | Created `Department` model, permission matrix, and administrative department CRUD endpoints. | Access faults when unassigned moderators logged in. Added null-check guards. | `Completed` |
| **W2 (07/13 – 07/19)** | Queue Routing | Implemented automatic complaint routing to department queues and master admin overview APIs. | Data access leaks across departments. Enforced `@PreAuthorize` department matching. | `Completed` |
| **W3 (07/20 – 07/26)** | Moderator UI | Developed moderator queue dashboards, Accept/Resolve controls, and mandatory remark logging. | Empty resolution remarks permitted. Enforced `@NotBlank` validation rules. | `Completed` |
| **W4 (07/27 – 08/02)** | Escalation Controls | Created escalation queue APIs, manual admin escalation overrides, and escalation notification triggers. | Duplicate escalation alerts sent. Added escalation state verification checks. | `Completed` |
| **W5 (08/03 – 08/09)** | Bulk & Audit Logs | Developed transactional bulk status update APIs, atomic batch processing, and system audit loggers. | Partial failure state corruption during bulk updates. Enforced atomic rollbacks. | `Completed` |
| **W6 (08/10 – 08/16)** | Performance KPIs | Built moderator resolution throughput metrics and aggregate JPQL queries computing department speed. | Query execution delays. Optimized JPQL queries using indexed JOIN projections. | `Completed` |
| **W7 (08/17 – 08/23)** | Account Controls | Created admin interface to activate, deactivate, or reassign moderator accounts. | Deactivated moderator sessions remaining active. Triggered session registry purge. | `Completed` |
| **W8 (08/24 – 08/30)** | Internal Notes | Designed `ComplaintNote` entity for internal staff messaging with strict role checks. | Internal notes visible to student users. Enforced strict authority filters. | `Completed` |
| **W9 (08/31 – 09/06)** | Excel Streaming | Developed streaming Apache POI report generator for administrative complaint exports. | Out-of-memory errors on large data exports. Streamed output in 100-row chunks. | `Completed` |
| **W10 (09/07 – 09/13)** | Data Isolation | Audited moderator privilege escalation risks and verified 100% department data isolation. | Data overlap bug on joint complaint categories. Refactored query predicates. | `Completed` |
| **W11 (09/14 – 09/20)** | Query Optimization | Added composite MySQL indexes on `department_id` and `status`, achieving sub-100ms dashboard speeds. | Slow query response under high concurrent load. Solved via composite indexing. | `Completed` |
| **W12 (09/21 – 09/27)** | Production Release | Deployed module to staging environment, executed administrative workflow tests, and completed handover. | Sidebar navigation alignment bugs. Refined CSS flexbox layout parameters. | `Completed` |
