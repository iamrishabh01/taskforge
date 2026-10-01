# Project proposal: TaskForge

**Problem:** small and mid-size teams juggle work across chat, spreadsheets, and email, with no clear ownership, permissions, or reporting.

**Users and roles:** Org Owner, Admin, Project Manager, Member, Viewer (read-only guest). Roles apply at the organization level, with project-level overrides.

| Layer | MVP (first) | Advanced (later) |
|---|---|---|
| Features | Auth, organizations, projects, tasks (status, assignee, priority, labels), Kanban board, comments, activity feed | Sprints and burndown, email and in-app notifications, attachments, full-text search, audit log, live updates |
| Data | users, organizations, memberships, projects, project_members, tasks, comments, labels, task_labels | sprints, attachments, activity_log, notifications |
| Backend | Node + Express (TypeScript), layered: routes, controllers, services, repositories | Background jobs (SLA-style reminders, emails), caching, rate limiting |
| Frontend | React + TypeScript, React Router, server-state library for API data | Optimistic updates, virtualization, code splitting |
| Database | PostgreSQL, migrations, seed data | Indexing and query tuning with EXPLAIN |
| Ops | Git workflow from day one | Docker, GitHub Actions CI/CD, cloud deployment (I'll justify the platform choice then) |

## Tech Stack
React, TypeScript, Node, Express, PostgreSQL, Docker.