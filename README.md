# Girija Sankar Panda

**Data engineering · MLOps · Platform engineering**

I build data pipelines and the platforms that run them — from ingestion and orchestration on
Azure and AWS, to Databricks lakehouses, to GPU infrastructure that serves ML workloads.

---

## Featured projects

### GPUaaS & TokenaaS platform
A platform for selling GPU compute and AI inference as a service, designed against a real RFQ.

- **GPU Service Manager (Go):** Kubernetes controllers that provision per-customer GPU nodes —
  shared tenants as namespaces, dedicated tenants as their own vCluster — with quota, capacity
  accounting, SSH access through a gateway, and JupyterLab per node.
- **Customer portal (Next.js, TypeScript):** GPU launch wizard, billing, usage and an operator
  console; real nodes are gated on KYC (Supabase auth with row-level security).
- **Local GPU data centre on kind:** simulated H100/A100/L40S nodes including MIG slices,
  Envoy Gateway, and an end-to-end test that launches a node, SSHes in and runs Python.
- Architecture decisions recorded as ADRs: per-SKU tenancy tiers, a single service contract into
  the data centre, and a cloud-to-on-prem private-link design.

`Go` `Kubernetes` `controller-runtime` `vCluster` `Next.js` `Supabase` `Terraform`
· Repository is private — happy to walk through it.

### StockIQ — India + US fundamental screener
Screens NSE and US stocks for high-quality compounders using free Yahoo Finance data.

- 100-point scoring on cash conversion (CFO/PAT), profit and revenue growth, debt/equity and
  working-capital cycle (inventory days, DSO, DPO).
- FastAPI backend with a 24-hour file cache; Next.js 14 + Recharts frontend.

`Python` `FastAPI` `yfinance` `Next.js` `TypeScript`

### Databricks lakehouse with Terraform and AWS Step Functions
An orders pipeline promoted across dev / QA / prod.

- Terraform creates account-level groups, a catalog per environment (`raw` and `curated`
  schemas) and the grant matrix in Unity Catalog.
- Ingestion job defined as a Databricks Asset Bundle; an AWS Step Functions state machine
  triggers the run, polls its status and branches on success or failure.

`Databricks` `Unity Catalog` `Terraform` `AWS Step Functions` `PySpark`

### Helsinki bus data pipeline
Data engineering on Helsinki public-transport bus data.
<!-- TODO: add a one-line description of what it ingests and produces, the stack, and a link. -->

---

## Other work

- **[Hydraulic flow simulator](https://github.com/girijaundefined/hydraluics)** — interactive
  web tool for pressure distribution, friction heating and pressure drop in pipes.
- **University robot network** — shares donated lab robots with students: FastAPI + PostgreSQL +
  Redis backend, WireGuard networking, and a sanitising cleanup protocol between sessions.
- **OpenFGA authorization demo** — visual, interactive walkthrough of relationship-based access
  control (ReBAC).
- **React Native app** — mobile app scaffold with Jest tests and a documented project workflow.

---

## Skills

| Area | Tools |
| --- | --- |
| Data engineering | Azure Data Factory, Databricks, PySpark, SQL, Delta Lake, batch and streaming pipelines |
| Cloud | AWS (Step Functions, S3, IAM), Azure |
| MLOps & platforms | Kubernetes, Docker, Terraform, GPU scheduling (NVIDIA Run:ai concepts, MIG), CI/CD |
| Backend | Python (FastAPI), Go, TypeScript (Node.js, Next.js), PostgreSQL, Redis |

---

📫 Reach me at **girija.undefined@gmail.com**
