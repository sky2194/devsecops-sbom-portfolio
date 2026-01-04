# DevSecOps SBOM & Vulnerability Analysis Portfolio Project

This project demonstrates an end-to-end DevSecOps workflow for generating
Software Bills of Materials (SBOMs) and performing dependency vulnerability
scanning across multi-stack applications using **Syft, CycloneDX, and Grype**.

The goal of the project is to showcase practical hands-on experience with
software supply-chain security, SBOM governance, and automated security scanning.

---

## 🎯 Objectives

- Generate SBOMs for multiple application stacks
- Use both **Syft SBOM** and **CycloneDX SBOM** formats
- Perform vulnerability scanning using **Grype**
- Compare findings from different SBOM types
- Organize results into a structured, auditable portfolio repository
- Document findings and security insights

---

## 🛠️ Technology Stack

| Category | Tools |
|--------|------|
| SBOM Generators | Syft, CycloneDX |
| Vulnerability Scanner | Grype |
| Languages / Platforms | Java, Python, Node.js |
| Package Managers | Maven, Pip, NPM |
| Environment | macOS / Linux |
| Version Control | Git & GitHub |

---

## 📦 Applications Analyzed

This project contains three sample applications:

| Project | Stack | Source Location |
|--------|------|----------------|
| `java-sample` | Java / Maven | `apps/java-sample/` |
| `python-sample` | Python venv / pip | `apps/python-sample/` |
| `ui-sample` | Node.js / npm | `apps/ui-sample/` |

Each project was scanned independently using the same DevSecOps workflow.

---

## 🔍 DevSecOps Workflow

The following steps were performed for each project:

1️⃣ Generate SBOM using **Syft (JSON SBOM)**  
2️⃣ Generate SBOM using **CycloneDX format**  
3️⃣ Run vulnerability scans using **Grype**  
4️⃣ Export results in
- JSON reports (machine-readable)
- Text / table reports (human-readable)

5️⃣ Store outputs in structured folders

---

## 📂 Repository Structure
apps/ # Application source projects
sboms/
├── java-sample/
├── python-sample/
└── ui-sample/
reports/
├── java-sample/
├── python-sample/
└── ui-sample/
README.md



### SBOM Files

Each project contains:

- `<project>-syft-sbom.json`
- `sbom-cyclonedx.json`

### Vulnerability Reports

Produced in two formats:

- `grype-*.json` → Automation / ingestion
- `grype-*.txt`  → Human readable report output

---

## 🧪 SBOM & Vulnerability Automation Script

A reusable automation script was implemented to:

- Generate SBOMs
- Run scans
- Export results
- Store per-project outputs

This ensures consistency and repeatability across scans.

---

## 📊 Vulnerability Findings Summary

> (Values depend on scan results — candidates will update as needed)

| Project | High | Medium | Low | Scanner Source |
|--------|------|-------|-----|---------------|
| java-sample | TBD | TBD | TBD | Grype |
| python-sample | 3 | 2 | 0 | Grype |
| ui-sample | TBD | TBD | TBD | Grype |

Key observations:

- Most issues related to outdated dependency versions
- Some vulnerabilities inherited transitively
- CycloneDX SBOM helped identify ecosystem relationships
- Syft SBOM provided detailed package-level metadata

---

## 🛡️ Security Remediation Approach

Actions recommended based on findings:

✔ Upgrade vulnerable dependencies  
✔ Replace unsupported library versions  
✔ Track risks using SBOM governance  
✔ Re-scan after remediation  
✔ Automate SBOM generation in CI/CD pipeline  

This project demonstrates a practical DevSecOps methodology for
software-supply-chain risk detection and dependency lifecycle management.

---

## ✅ Outcomes

This portfolio project demonstrates capability in:

- SBOM generation across multiple runtimes
- Supply-chain & dependency security analysis
- Running and interpreting vulnerability scans
- Structuring security reports for audit traceability
- Automating DevSecOps security workflows

---

## 📌 Future Enhancements

Planned improvements:

- Integrate into GitHub Actions CI pipeline
- Automate scheduled SBOM & Grype scans
- Add HTML dashboard reporting
- Map vulnerabilities to CVSS severity trend graphs

---

## 👤 Author

**Koutilya (Sky)**  
DevSecOps | Cloud Security | Application Security
