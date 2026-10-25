<div align="center">

<!-- Hero Dynamic Waving Banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:004e92,50:0078D4,100:00D2FF&height=260&section=header&text=SOURABH%20KUMAR&fontSize=54&fontColor=ffffff&animation=fadeIn&fontAlignY=36&desc=%E2%98%81%EF%B8%8F%20DevSecOps%20Engineer%20%7C%20Azure%20Cloud%20%7C%20Terraform%20%7C%20CI%2FCD%20Automation&descFontSize=19&descAlignY=58" width="100%" alt="Sourabh Kumar Header Banner" />

<!-- Dynamic Animated Typing Subtitle -->
<a href="https://github.com/iam-sourabhkumar">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=23&duration=2600&pause=900&color=00D2FF&center=true&vCenter=true&width=840&lines=DevSecOps+Engineer+%E2%80%A2+Bangalore%2C+India;Azure+Cloud+%26+Infrastructure+as+Code+with+Terraform;CI%2FCD+Pipelines+%E2%80%A2+Git+%26+GitHub+Workflows;Linux+Administration+%E2%80%A2+Shell+Automation;Shifting+Security+Left+in+Every+Pipeline" alt="Sourabh Kumar Typing SVG" />
</a>

<br />

<!-- Quick Navigation Bar -->
<p align="center">
  <a href="#about"><b>🧭 About</b></a> •
  <a href="#focus"><b>⚡ Focus</b></a> •
  <a href="#blueprints"><b>🏛️ Blueprints</b></a> •
  <a href="#arsenal"><b>🛠️ Arsenal</b></a> •
  <a href="#deepdives"><b>📂 Deep Dives</b></a> •
  <a href="#projects"><b>🌟 Projects</b></a> •
  <a href="#telemetry"><b>📊 Telemetry</b></a> •
  <a href="#connect"><b>💬 Connect</b></a>
</p>

<!-- Live Badges & Counters -->
<p align="center">
  <a href="https://komarev.com/ghpvc/?username=iam-sourabhkumar&style=for-the-badge&color=0078d4">
    <img src="https://komarev.com/ghpvc/?username=iam-sourabhkumar&style=for-the-badge&color=0078d4&label=PROFILE+VIEWS" alt="Profile Views" />
  </a>
  <a href="https://www.linkedin.com/in/sourabhkrdev/">
    <img src="https://img.shields.io/badge/LinkedIn-Sourabh%20Kumar-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <img src="https://img.shields.io/badge/Location-Bangalore%2C%20India-00C49F?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Location" />
  <img src="https://img.shields.io/badge/Focus-Azure%20%7C%20DevSecOps%20%7C%20Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white" alt="Focus" />
  <img src="https://img.shields.io/badge/Status-Open%20to%20Collaborate-28A745?style=for-the-badge" alt="Status" />
</p>

---

</div>

<a name="about"></a>
## 💻 Terminal Identity

```bash
┌──(sourabh㉿devsecops)-[~/cloud-platform]
└─$ ./run-pipeline-inspection.sh --cloud azure --iac terraform --mode shift-left

[✔] Infrastructure as Code: Terraform modules, remote state, reusable patterns
[✔] CI/CD Pipelines: Automated build, test, scan and deploy workflows
[✔] Security Gates: Secrets, IaC and image scanning wired into pull requests
[✔] Cloud Platform: Microsoft Azure (also exploring AWS with Terraform)
[✔] Linux & Shell: Fundamentals to system administration and scripting
[✔] Learning in Public: Documenting every concept in open repositories
```

> *"Automate the repeatable. Secure it early. Document what you learn."*

I'm **Sourabh Kumar**, a **DevSecOps Engineer** based in **Bangalore, India**. I work at the intersection of **cloud infrastructure, automation, and security**: provisioning Azure environments with **Terraform**, building **CI/CD pipelines**, and embedding security into every phase of the delivery lifecycle instead of bolting it on at the end.

I also build in public. My repositories are a mix of **production-style Terraform code** and **practical learning hubs** covering Linux, DevOps, and DevSecOps from zero to hero.

---

<a name="focus"></a>
## ⚡ What I Work On

<div align="center">

| Area | Focus | What it means in practice |
| :--- | :--- | :--- |
| ☁️ **Azure Cloud** | Infrastructure on Microsoft Azure | Designing and provisioning repeatable cloud environments. |
| ⚙️ **Infrastructure as Code** | Terraform (HCL) | Reusable modules, remote state, and automated provisioning. |
| 🔁 **CI/CD** | Pipeline automation | Automating build, validation, and deployment with Git-based workflows. |
| 🛡️ **DevSecOps** | Shift-left security | Integrating security checks into every stage of the DevOps lifecycle. |
| 🐧 **Linux** | Administration and scripting | Commands, permissions, networking, and shell scripting. |
| 📚 **Knowledge Sharing** | Open documentation | Turning real-world implementations into practical guides. |

</div>

---

<a name="blueprints"></a>
## 🏛️ Architectural Blueprints

### 1. Terraform-Driven Azure Delivery Flow

How infrastructure changes move from a commit to a running Azure environment, with validation and review at every step.

```mermaid
flowchart LR
    classDef trigger fill:#1E293B,stroke:#64748B,stroke-width:2px,color:#fff;
    classDef stage fill:#0F172A,stroke:#0284C7,stroke-width:2px,color:#fff;
    classDef sec fill:#450A0A,stroke:#DC2626,stroke-width:2px,color:#fff;
    classDef gate fill:#581C87,stroke:#9333EA,stroke-width:2px,color:#fff;
    classDef deploy fill:#0C4A6E,stroke:#0284C7,stroke-width:2px,color:#fff;

    DEV([👨‍💻 Developer Commit]):::trigger --> PR[🔀 Pull Request]:::trigger

    subgraph S1[" 📝 Validate "]
        FMT["terraform fmt"]:::stage
        VAL["terraform validate"]:::stage
    end

    subgraph S2[" 🛡️ Secure "]
        SEC["Secret & IaC Scanning"]:::sec
    end

    subgraph S3[" 📋 Plan "]
        PLAN["terraform plan<br/>(Remote State)"]:::stage
    end

    subgraph S4[" 🚦 Review "]
        APPROVE{"Peer Review & Approval"}:::gate
    end

    subgraph S5[" 🚀 Deploy "]
        APPLY["terraform apply"]:::deploy
        AZ["☁️ Microsoft Azure"]:::deploy
    end

    PR --> S1 --> S2 --> S3 --> S4
    S4 -->|Approved| APPLY --> AZ
```

---

### 2. DevSecOps: Security Across the Whole Lifecycle

```mermaid
flowchart LR
    classDef plan fill:#1E293B,stroke:#64748B,stroke-width:2px,color:#fff;
    classDef build fill:#0F172A,stroke:#0284C7,stroke-width:2px,color:#fff;
    classDef sec fill:#450A0A,stroke:#DC2626,stroke-width:2px,color:#fff;
    classDef ops fill:#064E3B,stroke:#059669,stroke-width:2px,color:#fff;

    P["📌 Plan<br/>Threat Modeling"]:::plan --> C["💻 Code<br/>Secret Scanning"]:::sec
    C --> B["🔨 Build<br/>Dependency Checks"]:::build
    B --> T["🧪 Test<br/>SAST / IaC Scans"]:::sec
    T --> R["📦 Release<br/>Image Scanning"]:::sec
    R --> D["🚀 Deploy<br/>Policy Checks"]:::build
    D --> O["📡 Operate<br/>Monitor & Respond"]:::ops
    O -.->|Feedback Loop| P
```

---

<a name="arsenal"></a>
## 🛠️ Technical Arsenal

<div align="center">

### ☁️ Cloud & Infrastructure
<a href="#">
  <img src="https://skillicons.dev/icons?i=azure,terraform,linux,bash&theme=dark" alt="Cloud Stack" />
</a>

<br />

![Microsoft Azure](https://img.shields.io/badge/Microsoft_Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Shell Scripting](https://img.shields.io/badge/Shell_Scripting-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)

---

### 🛡️ DevSecOps, CI/CD & Version Control
<a href="#">
  <img src="https://skillicons.dev/icons?i=git,github,githubactions&theme=dark" alt="DevSecOps Stack" />
</a>

<br />

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![CI/CD](https://img.shields.io/badge/CI%2FCD_Pipelines-0078D7?style=for-the-badge&logo=azure-devops&logoColor=white)
![DevSecOps](https://img.shields.io/badge/DevSecOps-DC2626?style=for-the-badge&logo=hackthebox&logoColor=white)

</div>

---

<a name="deepdives"></a>
## 📂 Deep Dives

<details>
<summary><b>⚙️ Terraform: How I Structure Infrastructure Code (Click to Expand)</b></summary>
<br />

* **Reusable Modules:** Break infrastructure into small, composable modules so the same pattern deploys consistently across environments.
* **Remote State:** Store state remotely with locking to keep teams safe from conflicting changes.
* **Multi-Cloud Awareness:** Patterns that apply to both Azure and AWS, with a focus on Azure.
* **CI/CD Integration:** Run `fmt`, `validate`, and `plan` automatically on pull requests before anything is applied.

</details>

<details>
<summary><b>🛡️ DevSecOps: Shifting Security Left (Click to Expand)</b></summary>
<br />

* **Catch Early:** Scan for leaked secrets and insecure IaC before code is merged.
* **Automate Gates:** Make security checks part of the pipeline rather than a manual step.
* **Least Privilege:** Prefer scoped identities and role-based access over broad permissions.
* **Feedback Loop:** Use findings from production monitoring to improve earlier stages.

</details>

<details>
<summary><b>🐧 Linux: Zero to Hero Learning Path (Click to Expand)</b></summary>
<br />

* **Fundamentals:** Filesystem, commands, and file management.
* **Access Control:** Users, groups, and permissions.
* **Networking:** Core networking concepts and troubleshooting tools.
* **Automation:** Shell scripting and system administration tasks.

</details>

---

<a name="projects"></a>
## 🌟 Featured Repositories

<div align="center">

| Repository | Tech Stack | Description |
| :--- | :--- | :--- |
| **[DevSecOps](https://github.com/iam-sourabhkumar/DevSecOps)** | `DevSecOps` `Security` | An approach to software development that integrates security into every phase of the DevOps lifecycle. |
| **[Terraform](https://github.com/iam-sourabhkumar/Terraform)** | `Terraform` `Azure` `AWS` | Production-ready Terraform for provisioning and managing cloud infrastructure: modules, state management, CI/CD integration, and best practices. |
| **[Monolithic-app](https://github.com/iam-sourabhkumar/Monolithic-app)** | `Terraform` `Azure` `HCL` | Terraform-based IaC project for deploying a monolithic application on Microsoft Azure with reusable modules and automated provisioning. |
| **[devops-insights](https://github.com/iam-sourabhkumar/devops-insights)** | `DevOps` `CI/CD` `HCL` | A practical knowledge hub for modern DevOps, Cloud, IaC, CI/CD, Automation, and DevSecOps practices. |
| **[Linux-Basic](https://github.com/iam-sourabhkumar/Linux-Basic)** | `Linux` `Shell` | A beginner-friendly Linux repo covering commands, permissions, networking, shell scripting, and sysadmin concepts. |
| **[infra](https://github.com/iam-sourabhkumar/infra)** | `Terraform` `HCL` | Infrastructure code repository. |

</div>

---

<a name="telemetry"></a>
## 📊 Live Telemetry & GitHub Metrics

<div align="center">

<!-- GitHub Achievements Trophy Case -->
<a href="https://github.com/iam-sourabhkumar">
  <img src="https://github-profile-trophy.vercel.app/?username=iam-sourabhkumar&theme=onedark&no-frame=true&no-bg=true&margin-w=4&row=1&column=7" alt="Sourabh Kumar Trophies" />
</a>

<br /><br />

<table border="0">
  <tr>
    <td width="50%">
      <img src="https://github-readme-stats.vercel.app/api?username=iam-sourabhkumar&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=00D2FF&icon_color=0078D4&text_color=c9d1d9" alt="GitHub Stats" width="100%" />
    </td>
    <td width="50%">
      <img src="https://github-readme-streak-stats.herokuapp.com/?user=iam-sourabhkumar&theme=tokyonight&hide_border=true&background=0d1117&stroke=00D2FF&ring=0078D4&fire=ff7b72&currStreakNum=00D2FF" alt="GitHub Streak" width="100%" />
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=iam-sourabhkumar&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=00D2FF&text_color=c9d1d9" alt="Top Languages" width="60%" />
    </td>
  </tr>
</table>

<!-- Live Activity Graph -->
<a href="https://github.com/iam-sourabhkumar">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=iam-sourabhkumar&theme=react-dark&hide_border=true&area=true" width="100%" alt="Contribution Graph" />
</a>

</div>

---

<a name="connect"></a>
## 💬 Let's Connect & Collaborate

I'm happy to connect with engineers and teams to talk about:
- ☁️ Building and automating **Azure infrastructure with Terraform**
- 🛡️ Adding **security gates to CI/CD pipelines**
- 🐧 **Linux and DevOps** learning paths
- 🤝 Collaborating on **open-source DevOps and DevSecOps** projects

<div align="center">

<p align="center">
  <a href="https://www.linkedin.com/in/sourabhkrdev/">
    <img src="https://img.shields.io/badge/LinkedIn-Sourabh%20Kumar-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  &nbsp;
  <a href="https://github.com/iam-sourabhkumar">
    <img src="https://img.shields.io/badge/GitHub-iam--sourabhkumar-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
</p>

<br />

<p align="center">
  <i>"If it has to be done twice, automate it. If it has to be trusted, secure it. If it has to be learned, document it."</i>
</p>

<p align="center">
  <strong>⭐ Star my repositories if you find them useful! ⭐</strong>
</p>

<!-- Dynamic Footer Wave -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00D2FF,50:0078D4,100:004e92&height=120&section=footer" width="100%" alt="Footer Wave" />

</div>
