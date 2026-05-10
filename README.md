#Hi, I'm Sharan Chenna

SRE · Platform Engineering · DevOps

4+ years operating large-scale Linux and cloud infrastructure. First hire on Oracle OCI's CloudOps SRE team — automated 15+ manual runbooks via a Python CLI, cutting alarm resolution time from 45+ minutes to under 10. Currently building production-grade open source tooling in AIOps, Kubernetes observability, and cloud-native reliability engineering.

me@sharanch.dev · [sharanch.dev](https://sharanch.dev) · Hyderabad, India

---

## Projects

**[log-explainer](https://github.com/sharanch/log-explainer)** — Python · Ollama · GitHub Actions · GHCR  
AIOps CLI that tails live logs and explains each line in plain English using a local LLM — no data leaves the host. Two-pass severity classifier, sliding-window spike detection, automated incident summaries. Ships as .deb/.rpm/.pkg/.msi via a three-workflow CI/CD pipeline.

**[go-sre-observatory](https://github.com/sharanch/go-sre-observatory)** — Go · Kubernetes · Prometheus · Grafana · Loki  
End-to-end observability stack on Kubernetes built around a Go microservice with RED metrics instrumentation and deliberate SLO-breach simulation. Alert pipeline wired end to end: Prometheus → Alertmanager → Slack with severity routing and runbook-linked definitions.

**[chatops](https://github.com/sharanch/chatops)** — React · Node.js · PostgreSQL · ArgoCD · Helm  
3-tier application on Kubernetes with full GitOps via ArgoCD — sub-2-minute deploy cycles. Modular Helm charts with per-environment overrides; multi-stage Alpine builds cut image size by ~60%.

**[istio-mesh-demo](https://github.com/sharanch/istio-mesh-demo)** — Istio · Kubernetes · FastAPI · Kiali · Grafana  
Service mesh with mTLS-encrypted traffic via Envoy sidecars and live canary traffic shifting (100/0 → 50/50 → 0/100). Fault injection validates frontend resilience under degraded backend conditions.

**[postgresql-ha-lab](https://github.com/sharanch/postgres-ha-resiliency-lab)** — CloudNativePG · Kubernetes  
HA PostgreSQL cluster with RPO < 5s and RTO < 30s, validated via chaos scenarios (pod kill, node drain). Zero data loss across 10+ failure events.

**[aws-security-auditor](https://github.com/sharanch/aws-security-best-practices)** — Boto3 · AWS  
Audits AWS environments against CIS benchmarks — surfaces IAM over-privilege, unrotated keys, and open S3 buckets and security groups.

---

## Stack

**Cloud & Infra** — Kubernetes · Docker · Helm · ArgoCD · OCI · AWS · Terraform · Linux · KVM  
**Observability** — Prometheus · Grafana · Alertmanager · Loki · Zabbix  
**Automation** — Python · Go · Bash · Ansible · GitHub Actions · Jenkins · Boto3  
**Reliability** — Incident command (P0/P1) · Post-mortems · SLO design · Chaos engineering

---

Open to SRE · Platform Engineer · DevOps Engineer roles. Reach me at me@sharanch.dev
