<!-- ═══════════════════════════ HEADER ═══════════════════════════ -->
<p align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0F2027,50:203A43,100:2F81F7&height=220&section=header&text=Amllan%20Bhukta&fontSize=64&fontColor=FFFFFF&animation=twinkling&fontAlignY=36&desc=DevOps%20Engineer%20%E2%80%A2%20Platform%20%E2%80%A2%20SRE%20%E2%80%A2%20AIOps&descSize=20&descAlignY=58" alt="Amllan Bhukta" />
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=2800&pause=700&color=2F81F7&center=true&vCenter=true&width=720&lines=%24+kubectl+get+engineer+amllan+-o+wide;Kubernetes+%E2%80%A2+AWS+%E2%80%A2+Terraform+%E2%80%A2+GitOps;Shipping+platforms+400%2B+developers+rely+on;Building+AIOps+%2B+MLOps+on+Amazon+Bedrock+%F0%9F%A4%96;Automate+the+toil.+Observe+everything.+%E2%9A%99%EF%B8%8F" alt="Typing intro" />
</p>

<p align="center">
  <a href="mailto:amllanbhukta123@gmail.com"><img src="https://img.shields.io/badge/Email-Contact%20me-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <a href="https://github.com/amllan123?tab=repositories"><img src="https://img.shields.io/badge/Repos-Explore-181717?style=for-the-badge&logo=github&logoColor=white" alt="Repositories" /></a>
  <img src="https://komarev.com/ghpvc/?username=amllan123&style=for-the-badge&color=2F81F7&label=PROFILE+VIEWS" alt="Profile views" />
</p>

---

## `$ whoami`

```console
$ kubectl get engineer amllan -o wide
NAME     ROLE              COMPANY   EXPERIENCE   STATUS    FOCUS
amllan   DevOps Engineer   Jar       2+ yrs       Running   K8s · AWS · GitOps · Observability · AIOps

$ kubectl describe engineer amllan | grep -A6 Spec
Spec:
  Builds:      Kubernetes platforms, GitOps pipelines, internal developer tooling
  Runs:        LLM gateway for 400+ developers (SSO, budgets, autoscaling)
  Believes:    toil should be automated, alerts should be actionable
  Learning:    SRE: SLOs, error budgets, incident response, Linux internals
  Building:    aiops-platform (from-scratch AIOps + MLOps on AWS)
  Location:    India 🇮🇳
```

## ⚡ Highlights

<table>
  <tr>
    <td width="50%" valign="top">

#### ☸️ Kubernetes platform
- Node autoscaling with **Karpenter** and workload scaling with **HPA**
- Per-team **staging namespaces** for isolated testing
- Safe rollouts with health probes and quick rollbacks

    </td>
    <td width="50%" valign="top">

#### 🔁 GitOps and developer platform
- **Argo CD** for declarative, Git-driven deployments
- **Backstage** self-service portal for developers
- Centralised secrets with **HashiCorp Vault**

    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">

#### 🤖 AI platform
- Runs an internal **LLM gateway (Bifrost)** for **400+ developers**
- SSO login, **per-user budgets**, and autoscaling (**HPA 20 → 50 pods**)
- Cost and usage visibility per team

    </td>
    <td width="50%" valign="top">

#### 💬 AI support bot
- A **CRM assistant** answering support questions with an LLM
- **Guardrails** scope every answer to the signed-in user's own data
- Blocks system-level and cross-user questions

    </td>
  </tr>
</table>

## 🛠️ Now building: `aiops-platform`

> A production-style **AIOps + MLOps** platform, built from zero, fully in Git:
> **detect → explain → fix (with human approval)**.

```mermaid
flowchart LR
    subgraph K8s["☸️ Kubernetes on AWS (Terraform + Argo CD)"]
        APP["Demo app<br/>with chaos switches"]
        OBS["Prometheus · Loki<br/>OpenTelemetry"]
        AM["Alertmanager"]
    end
    subgraph AI["🤖 AIOps layer"]
        DET["Log + metric<br/>anomaly detection"]
        ENR["AI alert enricher"]
        REM["Remediation agent<br/>(approval-based)"]
    end
    GW["Bifrost LLM gateway"] --> BR["Amazon Bedrock<br/>Claude · Titan"]
    APP --> OBS --> AM --> ENR
    OBS --> DET --> ENR
    ENR <--> GW
    ENR --> SL["💬 Slack"]
    SL -- "approve" --> REM --> APP
    DET -. "models tracked in" .-> ML["MLflow · Evidently"]
```

| Layer | Stack |
|:--|:--|
| **Infra** | Terraform · Kubernetes on AWS · GitHub Actions · Argo CD |
| **Observability** | Prometheus · Alertmanager · Grafana · Loki · OpenTelemetry |
| **LLM gateway** | Self-hosted Bifrost → Amazon Bedrock (Claude, Titan embeddings) |
| **AIOps** | AI alert enricher · log anomaly detection (Drain3) · approval-based remediation agent · LLM evals in CI |
| **MLOps** | MLflow registry · Evidently drift detection · automated retraining · shadow/canary model deploys |

## 🧰 Tech stack

<table align="center">
  <tr>
    <td align="center" width="170"><b>☁️ Cloud</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=aws,gcp,azure,cloudflare" alt="Cloud" />
    </td>
  </tr>
  <tr>
    <td align="center"><b>📦 Containers &amp; orchestration</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=docker,kubernetes" alt="Docker and Kubernetes" />
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/helm/helm-original.svg" height="48" alt="Helm" title="Helm" />&nbsp;
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/argocd/argocd-original.svg" height="48" alt="Argo CD" title="Argo CD" />&nbsp;
      <img src="https://raw.githubusercontent.com/aws/karpenter-provider-aws/main/website/static/logo.png" height="48" alt="Karpenter" title="Karpenter" />
    </td>
  </tr>
  <tr>
    <td align="center"><b>🏗️ IaC, config &amp; secrets</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=terraform,ansible" alt="Terraform and Ansible" />
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vault/vault-original.svg" height="48" alt="Vault" title="HashiCorp Vault" />
    </td>
  </tr>
  <tr>
    <td align="center"><b>🔁 CI/CD &amp; platform</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=githubactions,jenkins,gitlab,git,github" alt="CI/CD" />
      <img src="https://cdn.simpleicons.org/backstage" height="48" alt="Backstage" title="Backstage" />&nbsp;
      <img src="https://cdn.simpleicons.org/sonarqubeserver" height="48" alt="SonarQube" title="SonarQube" />&nbsp;
      <img src="https://cdn.simpleicons.org/trivy" height="48" alt="Trivy" title="Trivy" />
    </td>
  </tr>
  <tr>
    <td align="center"><b>📈 Observability</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=prometheus,grafana,elasticsearch" alt="Observability" />
      <img src="https://raw.githubusercontent.com/grafana/loki/main/docs/sources/logo.png" height="48" alt="Loki" title="Grafana Loki" />&nbsp;
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/opentelemetry/opentelemetry-original.svg" height="48" alt="OpenTelemetry" title="OpenTelemetry" />
    </td>
  </tr>
  <tr>
    <td align="center"><b>🐧 OS, scripting &amp; tooling</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=linux,ubuntu,bash,python,nginx,vim,vscode,postman" alt="OS and scripting" />
    </td>
  </tr>
  <tr>
    <td align="center"><b>🗄️ Data</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=postgres,mysql,mongodb,redis" alt="Databases" />
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/clickhouse/clickhouse-original.svg" height="48" alt="ClickHouse" title="ClickHouse" />
    </td>
  </tr>
  <tr>
    <td align="center"><b>🤖 AI &amp; MLOps</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=fastapi,flask" alt="FastAPI and Flask" />
      <img src="https://cdn.simpleicons.org/anthropic/D97757" height="48" alt="Claude on Amazon Bedrock" title="Claude on Amazon Bedrock" />&nbsp;
      <img src="https://cdn.simpleicons.org/googlecloud" height="48" alt="Vertex AI" title="Vertex AI" />&nbsp;
      <img src="https://cdn.simpleicons.org/mlflow" height="48" alt="MLflow" title="MLflow" />
    </td>
  </tr>
  <tr>
    <td align="center"><b>🌐 Web (MERN)</b></td>
    <td>
      <img src="https://skillicons.dev/icons?i=nodejs,express,react,nextjs,js,ts,html,css" alt="Web" />
    </td>
  </tr>
</table>

## 📌 Featured repositories

| Repository | What it is |
|:--|:--|
| 🚨 [**Scoutflo-SRE-Playbooks**](https://github.com/amllan123/Scoutflo-SRE-Playbooks) | Incident-response playbooks for AWS and Kubernetes: step-by-step guides for on-call engineers |
| 🧪 [**DevOps-Projects**](https://github.com/amllan123/DevOps-Projects) | Real-world DevOps projects, from beginner to advanced |
| 📈 [**Microservice-Monitroing**](https://github.com/amllan123/Microservice-Monitroing) | Monitoring stack for a microservices application |
| ⚙️ [**k8s-Ansible**](https://github.com/amllan123/k8s-Ansible) | Ansible automation to bootstrap a Kubernetes cluster |
| ☁️ [**EKS_Terraform**](https://github.com/amllan123/EKS_Terraform) | Amazon EKS provisioned with Terraform |

## 📊 GitHub stats

<p align="center">
  <img height="170" src="https://github-readme-stats.vercel.app/api?username=amllan123&show_icons=true&hide_border=true&bg_color=00000000&title_color=2F81F7&icon_color=2F81F7&text_color=7D8590&ring_color=2F81F7" alt="GitHub stats" />
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=amllan123&layout=compact&hide_border=true&bg_color=00000000&title_color=2F81F7&text_color=7D8590" alt="Top languages" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=amllan123&hide_border=true&background=00000000&ring=2F81F7&fire=FF6B35&currStreakLabel=2F81F7&sideLabels=7D8590&currStreakNum=7D8590&sideNums=7D8590&dates=7D8590" alt="GitHub streak" />
</p>

## 🐍 Contribution snake

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/amllan123/amllan123/output/github-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/amllan123/amllan123/output/github-snake.svg" />
    <img alt="Contribution snake animation" src="https://raw.githubusercontent.com/amllan123/amllan123/output/github-snake.svg" />
  </picture>
</p>

<!-- ═══════════════════════════ FOOTER ═══════════════════════════ -->
<p align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:2F81F7,50:203A43,100:0F2027&height=120&section=footer" alt="footer" />
</p>
