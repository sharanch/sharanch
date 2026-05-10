# Hi, I'm Sharan

I like understanding how things work — what happens when a kernel panics, why a distributed system splits, how a hypervisor schedules compute across bare metal. That curiosity is what pulled me into SRE and keeps me there.

4 years of operating infrastructure at scale — 2,500+ Linux servers at CtrlS, then OCI Compute at Oracle. I've been paged at 2am, dug through logs I didn't write, and learned that most incidents aren't mysterious — they're just noisy.

Most engineers inherit systems. I'd rather build them first so I know what I'm inheriting.

---

## Projects

**[log-explainer](https://github.com/sharanch/log-explainer)** — Python · Ollama · GitHub Actions · GHCR

*During incidents at Oracle I was constantly switching between log viewers, documentation, and AI assistants — copy-pasting to make sense of what was happening. Built this so you can just tail logs over SSH and get plain English explanations locally, without breaking focus or sending data anywhere.*

Local LLM-powered log explainer with two-pass severity classification, sliding-window spike detection, and automated incident summaries. Ships as .deb/.rpm/.pkg/.msi via a three-workflow CI/CD pipeline.

---

**[go-sre-observatory](https://github.com/sharanch/go-sre-observatory)** — Go · Kubernetes · Prometheus · Grafana · Loki

*Most engineers never get to build an alerting system from scratch — they inherit one. This is me building one end to end so I actually understand every piece of it.*

Full observability stack on Kubernetes with RED metrics instrumentation, deliberate SLO-breach simulation, and an alert pipeline wired all the way through: Prometheus → Alertmanager → Slack with severity routing and runbook-linked definitions.

---

**[chatops](https://github.com/sharanch/chatops)** — React · Node.js · PostgreSQL · ArgoCD · Helm

*GitOps and single source of truth get thrown around a lot. Built this to demonstrate what they actually mean in practice — every change through Git, ArgoCD reconciles the rest.*

3-tier app on Kubernetes with full GitOps via ArgoCD — sub-2-minute deploy cycles, modular Helm charts with per-environment overrides, path-based CI that only rebuilds affected services.

---

**[istio-mesh-demo](https://github.com/sharanch/istio-mesh-demo)** — Istio · Kubernetes · FastAPI · Kiali · Grafana

*Kubernetes is a vast space and service mesh is one of the parts most engineers skip. Built this to get hands-on with secure service-to-service communication — mTLS, traffic shaping, and what resilience actually looks like under fault injection.*

mTLS-encrypted traffic via Envoy sidecars with live canary shifting (100/0 → 50/50 → 0/100) and fault injection to validate frontend resilience under degraded backend conditions.

---

**[postgresql-ha-lab](https://github.com/sharanch/postgres-ha-resiliency-lab)** — CloudNativePG · Kubernetes

*Wanted to define SLIs and SLOs for a stateful system and actually measure them — not just write them down. Chaos scenarios make the error budget concrete.*

HA PostgreSQL cluster with RPO < 5s and RTO < 30s, validated via automated chaos (pod kill, node drain). Zero data loss across 10+ failure events.

---

**[aws-security-auditor](https://github.com/sharanch/aws-security-best-practices)** — Boto3 · AWS

*Was studying for AWS SAA and kept reading the Well-Architected Framework thinking "how would you actually audit this?" Security and system design are the same problem at different layers.*

CIS benchmark auditor for AWS environments — surfaces IAM over-privilege, unrotated keys, and open S3 buckets and security groups.

---

## Stack

Kubernetes · Prometheus · Grafana · Terraform · Ansible · Python · Go · Bash  
OCI · AWS · ArgoCD · Helm · Loki · Alertmanager · Linux · Docker

---

me@sharanch.dev · [sharanch.dev](https://sharanch.dev) · Open to SRE and Platform Engineering roles
