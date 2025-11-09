# ☁️ Terraform Codespaces — Hands-On Labs by Adnan Ahmed

Welcome to the **Terraform Codespaces Labs** — a hands-on learning environment designed for engineers and architects who want to build a strong foundation in Terraform using practical, guided examples.  

This repository is inspired by the Terraform Codespaces concept created by Bryan Krausen and reimagined here with updated content, structure, and examples.  
All labs are designed to run seamlessly inside **GitHub Codespaces** or locally in **VS Code**.  

---

## 🚀 What You’ll Learn  

These labs walk you step-by-step through Terraform fundamentals and advanced workflows.  
You’ll explore topics such as:  

- Terraform language and configuration syntax  
- Variables, expressions, and dependencies  
- Working with providers and resources  
- Functions, modules, and dynamic code  
- Managing state and data sources  
- Deploying infrastructure across multiple clouds  

Each lab contains clear explanations, Terraform code, and cleanup instructions to help you learn by doing.  

---

## 🧱 Repository Structure  

terraform-codespaces-adnan/
│
├── 01-variables/
├── 02-providers/
├── 03-resources/
├── 04-functions/
├── 05-expressions/
├── 06-provisioners/
└── 99-advanced/

yaml
Copy code

Each folder represents a concept-based learning area and includes:  
- Example Terraform configuration (`main.tf`, `variables.tf`, `outputs.tf`)  
- Inline documentation and explanations  
- Lab README with details, commands, and cleanup steps  

---

## 🧩 Prerequisites  

Before you begin, make sure you have:  

- **Terraform CLI** v1.6 or later  
- **GitHub Codespaces** or **VS Code** installed locally  
- Optional: AWS or Azure account for provider testing  
- Recommended extensions:  
  - [Terraform VS Code Extension](https://marketplace.visualstudio.com/items?itemName=HashiCorp.terraform)  
  - [GitHub Codespaces](https://github.com/features/codespaces)  

---

## ▶️ Getting Started  

### 🔹 Run in GitHub Codespaces  
Click below to open your own Codespace instantly 👇  

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=<your-repo-id>)

---

### 🔹 Run Locally  

Clone and initialize your environment:  

```bash
git clone https://github.com/<your-username>/terraform-codespaces-adnan.git
cd terraform-codespaces-adnan
terraform init
terraform plan
terraform apply
When finished, destroy all resources safely:

bash
Copy code
terraform destroy -auto-approve
🧠 HashiCorp Terraform Basics 💻
Labs 1–5 are the foundation of Terraform learning and should be completed in order, as each lab builds upon the previous one.

#	Lab Name	AWS	Azure	GitHub
1	Getting Started with Terraform	AWS	Azure	GitHub
2	Create Your First Resource	AWS	Azure	GitHub
3	Working with Variables and Dependencies	AWS	Azure	GitHub
4	Managing Multiple Resources	AWS	Azure	GitHub
5	Working with State, Data Sources, and the CLI	AWS	Azure	GitHub

✨ Making Code More Dynamic and Reusable ✨
Labs 6–11 focus on creating efficient, reusable, and scalable Terraform code.
These labs are independent and can be completed in any order.

#	Lab Name	AWS	Azure	GitHub
6	Making Code Dynamic and Reusable	AWS	Azure	GitHub
7	Simplify Code with local Values	AWS	Azure	GitHub
8	Create Multiple Resources with count	AWS	Azure	GitHub
9	Deploy Multiple Resources with for_each	AWS	Azure	GitHub
10	Managing Explicit Dependencies with depends_on	AWS	Azure	GitHub
11	Using Multiple Providers for Multiple Regions	AWS	Azure	GitHub

🧩 Advanced Terraform Labs 🚀
Labs 12–17 cover advanced scenarios and real-world use cases that extend beyond core Terraform concepts.

#	Lab Name	AWS	Azure	GitHub
12	Create and Use Terraform Modules	AWS	Azure	GitHub
13	Automate Resource Lifecycle with depends_on	AWS	Azure	GitHub
14	Using Data Sources Across Environments	AWS	Azure	GitHub
15	Remote State and Backend Configuration	AWS	Azure	GitHub
16	Integrating Terraform with CI/CD	AWS	Azure	GitHub
17	Complete Infrastructure Deployment Scenario	AWS	Azure	GitHub

💡 Learning Flow
Each lab includes:

Concept Overview

Code Samples (main.tf, variables.tf, outputs.tf)

Terraform Commands (init, plan, apply)

Expected Output & Explanation

Cleanup Steps

This format ensures you learn why and how Terraform works — not just what to type.

🧾 Best Practices
Run terraform fmt before every commit

Validate your configuration with terraform validate

Use .tfvars files for environment-specific settings

Store Terraform state remotely for team collaboration

Apply least-privilege IAM policies when using cloud providers

🏗️ Contributing
Pull requests, new labs, and improvements are welcome!
If you’d like to add a lab (AWS, Azure, or generic), fork the repo and submit a PR.

📜 License
This project is licensed under the MIT License.
Feel free to reuse, modify, or extend it for your own learning or internal training.

🙌 Acknowledgments
Special thanks to:

Bryan Krausen for his original Terraform Codespaces concept

HashiCorp for Terraform and its open documentation

The cloud community for continuous innovation and sharing

“The best way to learn Terraform is to build, break, and rebuild — until you understand every block.” ☁️

yaml
Copy code

---
