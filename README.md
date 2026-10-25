# 3. `campuspulse-admin-moderator` (Member 3)

Save the following content as `README.md` inside the `campuspulse-admin-moderator` repository:

```markdown
# 🛡️ CampusPulse — Moderator & Admin Management Module

[![Spring Boot](https://img.shields.io/badge/Spring--Boot-3.x-brightgreen.svg)](https://spring.io/projects/spring-boot)
[![Apache POI](https://img.shields.io/badge/Reporting-Apache_POI-blue.svg)](https://poi.apache.org/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-blue.svg)](https://www.mysql.com/)

## 📌 Module Overview
The **Moderator & Admin Management** module equips administrative staff and department moderators with tools to manage incoming campus issues. Features include automated department queue assignment, moderator review dashboards, manual escalation overrides, atomic bulk status updating, internal ticket notes, system audit logging, and streaming Excel/CSV report exports.

---

## 🏗️ Repository Architecture & Directory Structure

```text
campuspulse-admin-moderator/
├── src/main/java/com/campuspulse/admin/
│   ├── controller/         # AdminController, ModeratorController, ReportController
│   ├── dto/                # BulkStatusUpdateDTO, ReportFilterDTO, NoteDTO
│   ├── entity/             # Department.java, AuditLog.java, ComplaintNote.java
│   ├── repository/         # DepartmentRepository, AuditRepository, NoteRepository
│   └── service/            # QueueRoutingService, EscalationService, ReportExportService
├── src/main/resources/
│   ├── templates/admin/    # Moderator queues, Admin panel, Department assignment
│   └── static/css/         # Admin dashboard theme & control panel layouts
├── Dockerfile
├── pom.xml
└── README.md
