<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=180&section=header&text=Girija%20Sankar%20Panda&fontColor=ffffff&fontSize=40&fontAlignY=36&desc=Solution%20Architect%20%C2%B7%20Data%20Engineering%20%C2%B7%20MLOps%20%C2%B7%20Platform%20Engineering&descAlignY=58&descSize=16" alt="Girija Sankar Panda — Solution Architect · Data Engineering · MLOps · Platform Engineering" width="100%" />

I build data pipelines and the platforms that run them — from ingestion and orchestration on
Azure and AWS, to Databricks lakehouses, to GPU infrastructure that serves ML workloads.

<a href="mailto:girija.undefined@gmail.com"><img src="https://img.shields.io/badge/Email-girija.undefined%40gmail.com-0f2027?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>

</div>

---

## 🛠️ Tech stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,go,ts,nextjs,react,fastapi&theme=dark" alt="Languages and frameworks" /><br/>
  <img src="https://skillicons.dev/icons?i=kubernetes,docker,terraform,aws,azure,githubactions&theme=dark" alt="Cloud and platforms" /><br/>
  <img src="https://skillicons.dev/icons?i=postgres,redis,supabase,linux,git&theme=dark" alt="Data stores and tools" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white" alt="Databricks" />
  <img src="https://img.shields.io/badge/Azure%20Data%20Factory-0078D4?style=flat-square&logo=microsoftazure&logoColor=white" alt="Azure Data Factory" />
  <img src="https://img.shields.io/badge/PySpark-E25A1C?style=flat-square&logo=apachespark&logoColor=white" alt="PySpark" />
  <img src="https://img.shields.io/badge/LightGBM-2E7D32?style=flat-square" alt="LightGBM" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" alt="scikit-learn" />
  <img src="https://img.shields.io/badge/AWS%20Step%20Functions-FF4F8B?style=flat-square&logo=awslambda&logoColor=white" alt="AWS Step Functions" />
</p>

---

## 🚀 Featured projects

### ⚡ GPUaaS & TokenaaS platform
> A platform for selling GPU compute and AI inference as a service, designed against a real RFQ.

- **GPU Service Manager (Go)** — Kubernetes controllers that provision per-customer GPU nodes:
  shared tenants as namespaces, dedicated tenants as their own vCluster, with quota, capacity
  accounting, SSH access through a gateway, and JupyterLab per node.
- **Customer portal (Next.js, TypeScript)** — GPU launch wizard, billing, usage and an operator
  console; real nodes are gated on KYC (Supabase auth with row-level security).
- **Local GPU data centre on kind** — simulated H100/A100/L40S nodes including MIG slices,
  Envoy Gateway, and an end-to-end test that launches a node, SSHes in and runs Python.
- **Architecture as ADRs** — per-SKU tenancy tiers, a single service contract into the data
  centre, and a cloud-to-on-prem private-link design.

`Go` `Kubernetes` `controller-runtime` `vCluster` `Next.js` `Supabase` `Terraform`
&nbsp;·&nbsp; 🔒 *Private repository — happy to walk through it.*

### 🤖 [ACS SNAP MLOps pipeline](https://github.com/girijaundefined/task-ml-ops)
> End-to-end ML pipeline predicting SNAP (food assistance) receipt from US Census ACS PUMS 2018–2022 data.

| Accuracy | ROC-AUC | Lift @ top 10% | Data |
| :---: | :---: | :---: | :---: |
| **90.1%** | **0.876** | **4.64×** | 59,048 Arkansas households · 18 features |

- LightGBM model, reproducible from config: `make` targets, a CLI, a FastAPI serving API,
  a Docker image, GitHub Actions CI and pre-commit checks.

`Python` `LightGBM` `scikit-learn` `FastAPI` `Docker` `GitHub Actions`

### 📈 StockIQ — India + US fundamental screener
> Screens NSE and US stocks for high-quality compounders using free Yahoo Finance data.

- 100-point scoring on cash conversion (CFO/PAT), profit and revenue growth, debt/equity and
  working-capital cycle (inventory days, DSO, DPO).
- FastAPI backend with a 24-hour file cache; Next.js 14 + Recharts frontend.

`Python` `FastAPI` `yfinance` `Next.js` `TypeScript`

### 🧱 Databricks lakehouse with Terraform and AWS Step Functions
> An orders pipeline promoted across dev / QA / prod.

- Terraform creates account-level groups, a catalog per environment (`raw` and `curated`
  schemas) and the grant matrix in Unity Catalog.
- Ingestion job defined as a Databricks Asset Bundle; an AWS Step Functions state machine
  triggers the run, polls its status and branches on success or failure.

`Databricks` `Unity Catalog` `Terraform` `AWS Step Functions` `PySpark`

### 🚌 Helsinki bus data pipeline
> Data engineering on Helsinki public-transport bus data.
<!-- TODO: add a one-line description of what it ingests and produces, the stack, and a link. -->

---

## 🧩 Other work

| Project | What it is |
| --- | --- |
| 💧 [Hydraulic flow simulator](https://github.com/girijaundefined/hydraluics) | Interactive web tool for pressure distribution, friction heating and pressure drop in pipes |
| 🤝 University robot network | Shares donated lab robots with students — FastAPI, PostgreSQL, Redis, WireGuard, and a sanitising cleanup protocol between sessions |
| 🔐 OpenFGA authorization demo | Visual, interactive walkthrough of relationship-based access control (ReBAC) |
| 📱 React Native app | Mobile app scaffold with Jest tests and a documented project workflow |

---

## 🧰 Skills

| Area | Tools |
| --- | --- |
| **Data engineering** | Azure Data Factory, Databricks, PySpark, SQL, Delta Lake, batch and streaming pipelines |
| **Cloud** | AWS (Step Functions, S3, IAM), Azure |
| **MLOps & platforms** | Kubernetes, Docker, Terraform, GPU scheduling (NVIDIA Run:ai concepts, MIG), CI/CD |
| **Backend** | Python (FastAPI), Go, TypeScript (Node.js, Next.js), PostgreSQL, Redis |

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:2c5364,50:203a43,100:0f2027&height=100&section=footer" alt="" width="100%" />
