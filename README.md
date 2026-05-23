# Hi, I'm Sharan

I like understanding how things work — what happens when a kernel panics, why a distributed system splits, how a hypervisor schedules compute across bare metal. That curiosity is what pulled me into SRE and keeps me there.

4 years of operating infrastructure at scale — 2,500+ Linux servers at CtrlS, then OCI Compute at Oracle. I've been paged at 2am, dug through logs I didn't write, and learned that most incidents aren't mysterious — they're just noisy.

Most engineers inherit systems. I'd rather build them first so I know what I'm inheriting.

**Currently: open to SRE and Platform Engineering roles · building · Hyderabad · open to remote**

---

## Built from real problems

**[log-explainer](https://github.com/sharanch/log-explainer)** — Python · Ollama · Elasticsearch · Filebeat · Kibana · GitHub Actions · GHCR

*During incidents at Oracle I was constantly switching between log viewers, documentation, and AI assistants — copy-pasting to make sense of what was happening. Built this so you can tail logs over SSH and get plain English explanations locally, without breaking focus or sending data anywhere.*

Local LLM-powered log explainer. Two-pass severity classification, spike detection, automated incident summaries. Ships as .deb/.rpm/.pkg/.msi via a three-workflow CI/CD pipeline. ELK integration (`--elk-output`) ships LLM-enriched explanations to Elasticsearch via Filebeat — raw logs and AI context queryable together in Kibana.

---

**[inkwell-complete](https://github.com/sharanch/inkwell-complete)** — Go · React · Kubernetes · ArgoCD · Istio · PostgreSQL · Redis · GitHub Actions

*Most microservices demos are toy services that share a database and call it distributed. Wanted to build one that actually enforces service boundaries — separate databases, gateway-level auth, real K8s infra patterns.*

Privacy-first blogging platform on Go microservices — API gateway, auth, blog, feed, and notify services, each with its own Postgres instance. Passwordless OTP auth with Redis TTL. K8s deployment with production-pattern manifests: HPA, PDB, mTLS via Istio, cert-manager, ArgoCD GitOps. Prometheus RED metrics on the gateway.

---

**[go-sre-observatory](https://github.com/sharanch/go-sre-observatory)** — Go · Kubernetes · Prometheus · Grafana · Loki

*Most engineers never get to build an alerting system from scratch — they inherit one. This is me building one end to end so I actually understand every piece.*

Full observability stack on Kubernetes. RED metrics, SLO-breach simulation, alert pipeline wired end to end: Prometheus → Alertmanager → Slack with severity routing and runbook-linked definitions.

---

**[postgres-ha-lab](https://github.com/sharanch/postgres-ha-resiliency-lab)** — CloudNativePG · Kubernetes · Prometheus · Grafana

*Wanted to define SLIs and SLOs for a stateful system and actually measure them under failure — not just write them down.*

HA PostgreSQL cluster with RPO < 5s and RTO < 30s, validated via automated chaos scenarios. Includes a custom Grafana SLO dashboard and error budget burn rate alerting. Zero data loss across 10+ failure events — with honest failure data documented.

---

**[chatops](https://github.com/sharanch/chatops)** — React · Node.js · PostgreSQL · ArgoCD · Helm

*GitOps and single source of truth get thrown around a lot. Built this to demonstrate what they actually mean — every change through Git, ArgoCD reconciles the rest.*

3-tier app on Kubernetes. Sub-2-minute deploy cycles, path-based CI, non-root containers, graceful shutdown, separate liveness and readiness probes.

---

**[istio-mesh-demo](https://github.com/sharanch/istio-mesh-demo)** — Istio · Kubernetes · FastAPI · Kiali · Grafana

*Kubernetes is a vast space and service mesh is one of the parts most engineers skip. Built this to get hands-on with secure service-to-service communication.*

mTLS via Envoy sidecars, zero application code changes. Live canary shifting (100/0 → 50/50 → 0/100) and fault injection to validate frontend resilience under degraded backend conditions.

---

**[networking-troubleshooting-runbooks](https://github.com/sharanch/networking-troubleshooting-runbooks)** — Linux · TCP · tcpdump · Python

*Most networking runbooks tell you what commands to run. These explain what's actually happening in the kernel and why.*

7 TCP failure scenarios simulated on Linux — connection refused, timeout, CLOSE_WAIT accumulation, TIME_WAIT exhaustion, retransmissions, port exhaustion, stale keepalives. Each one: what it looks like, why it happens, how to debug it, how to fix it.

---

**[aws-security-best-practices](https://github.com/sharanch/aws-security-best-practices)** — Boto3 · AWS · Bash

*Was studying for AWS SAA and kept reading the Well-Architected Framework thinking "how would you actually audit this?" Security and system design are the same problem at different layers.*

CIS benchmark coverage across 8 domains — IAM, EC2, VPC, CI/CD, S3, Lambda, RDS, detection and response. Audit scripts that exit with code 1 on critical findings, safe to use as CI/CD gates.

---

**[operations-autobot](https://github.com/sharanch/operations-autobot)** — Python · Ansible · Jira API

*The actual incident response CLI I built at Oracle — anonymised. Alarm fires in Slack, engineer copies the Jira ID, runs one command. Tool fetches the ticket, identifies the alarm type, runs the right Ansible playbook, posts the mitigation comment, assigns and transitions the ticket. What used to take 45+ minutes averaged under 10.*

Anonymised version of a production tool. The original automated 15+ runbooks across the OCI Compute CloudOps team.

---

## Stack

Kubernetes · Prometheus · Grafana · Terraform · Ansible · Python · Go · Bash  
OCI · AWS · ArgoCD · Helm · Loki · Alertmanager · Elasticsearch · Filebeat · Kibana  
Linux · Docker · Istio

---

me@sharanch.dev · [sharanch.dev](https://sharanch.dev) · Open to SRE and Platform Engineering roles · Hyderabad · Open to remote
