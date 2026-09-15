|  Ordre | Étape DevSecOps            | Outil            | Sécurité associée                    |
| -----: | -------------------------- | ---------------- | ------------------------------------ |
|  **1** | 📝 Plan                    | `claude`         | Security by Design / Threat Modeling |
|  **2** | 💻 Code                    | `git`            | Source Code Security / SCM           |
|  **3** | 🔐 Code Security           | `gitleaks`       | Secrets Security                     |
|  **4** | 🛡️ Code Security          | `semgrep`        | SAST                                 |
|  **5** | 🐍 Build / Test            | `python3`        | Dependency & Runtime Security        |
|  **6** | 🐳 Build                   | `docker`         | Container Security                   |
|  **7** | ⚙️ Test / Integration      | `docker compose` | Container Configuration Security     |
|  **8** | 🔎 Security Test           | `trivy`          | Vulnerability / Container Scanning   |
|  **9** | 🏗️ Infrastructure         | `terraform`      | Infrastructure as Code               |
| **10** | ☁️ Infrastructure Security | `checkov`        | IaC / Cloud Security                 |
| **11** | 🚀 Release / Deploy        | —                | Deployment Security                  |
| **12** | 🔄 Operate / Monitor       | —                | Runtime / Monitoring Security        |







| #      | Situation                                                            | Probabilité | Impact |  Score | Étiquette               |
| ------ | -------------------------------------------------------------------- | ----------: | -----: | -----: | ----------------------- |
| **3**  | SQL Injection dans la recherche de tâches                            |           5 |      5 | **25** | 🔴 **CRITIQUE**         |
| **9**  | Clé d'API laissée dans un ancien commit Git                          |           5 |      5 | **25** | 🔴 **CRITIQUE**         |
| **5**  | Port 5000 exposé sur `0.0.0.0`                                       |           5 |      4 | **20** | 🔴 **CRITIQUE**         |
| **8**  | Ancien salarié dont les accès n'ont jamais été révoqués              |           4 |      5 | **20** | 🔴 **CRITIQUE**         |
| **7**  | Bibliothèque tierce obsolète avec faille publiée                     |           4 |      5 | **20** | 🔴 **CRITIQUE**         |
| **12** | Employé qui clique sur une pièce jointe piégée                       |           4 |      5 | **20** | 🔴 **CRITIQUE**         |
| **2**  | Attaquant qui scanne Internet à la recherche de serveurs vulnérables |           5 |      3 | **15** | 🟠 **ÉLEVÉ**            |
| **1**  | Base de données des utilisateurs de TaskFlow                         |           3 |      5 | **15** | 🟠 **ÉLEVÉ**            |
| **11** | Code source de l'application                                         |           3 |      4 | **12** | 🟠 **ÉLEVÉ**            |
| **4**  | Mots de passe stockés hachés avec bcrypt                             |           2 |      5 | **10** | 🟡 **MOYEN / CONTRÔLE** |
| **6**  | Scan Trivy bloquant le pipeline sur CVE critique                     |           2 |      3 |  **6** | 🟡 **CONTRÔLE**         |
| **10** | 2FA activée sur les comptes GitHub                                   |           1 |      4 |  **4** | 🟢 **CONTRÔLE POSITIF** |
