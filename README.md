# ⚡ Energy Tracker

**Energy Tracker** is a backend platform designed to help organizations monitor and manage energy usage across multiple projects, meters, and customers. Built with Supabase and PostgreSQL, it supports structured data collection, relational mapping, and role-based access.

---

## 🏗️ Tech Stack

- [Supabase](https://supabase.com/) — open-source Firebase alternative (PostgreSQL, Auth, Realtime)
- Supabase CLI for local development and migrations
- PostgreSQL (hosted by Supabase)
- Terraform/OpenTofu for infrastructure provisioning (optional)

---

## 🗃️ Database Schema Overview

### Tables

#### `organizations`
Top-level entity representing an energy provider or client company.

| Column     | Type         | Description                        |
|------------|--------------|------------------------------------|
| `id`       | `int8`       | Primary key                        |
| `created_at` | `timestamptz` | Record creation timestamp         |
| `name`     | `text`       | Organization name                  |

---

#### `projects`
A project under an organization — could represent a facility, building, or regional site.

#### `customers`
Represents energy users or clients tied to a project or organization.

#### `meters`
Device-level table — each row likely represents a physical energy meter collecting consumption data.

#### `profiles`
User profiles, typically linked to Supabase Auth. Could support admin/staff/customer roles.

---

## 🚀 Quick Start

### 1. Clone & Install Supabase CLI

```bash
npm install -g supabase
