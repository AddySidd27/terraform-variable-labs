![Terraform](https://img.shields.io/badge/Terraform-Labs-blueviolet?logo=terraform)
![Status](https://img.shields.io/badge/Status-In_Progress-yellow)

# 🌍 Terraform Variable Labs — Zero to Hero Series

Welcome to the **Terraform Variable Labs** repository by *Adnan A Siddiqui*.  
This series is designed to help learners and cloud professionals **master Terraform variables** with real-world practical examples.

---

## 🧭 About This Series

Each variable type (String, List, Map, Boolean, Object) contains **50 labs**, divided into three categories:

- **Basic:** Foundational syntax and examples  
- **Intermediate:** Practical variable usage in real infrastructure  
- **Advanced:** Real-world automation scenarios and nested structures  

---

## 📂 Repository Structure

| Folder | Description |
|--------|--------------|
| **01-Strings** | Labs covering string interpolation, concatenation, defaults, and conditionals |
| **02-Lists** | Understanding lists, indexing, and using `count` and `for_each` with lists |
| **03-Maps** | Key-value pair handling, dynamic tagging, and structured configurations |
| **04-Conditionals** | If-Else, ternary expressions, and dynamic decisions |
| **05-Objects** | Complex and nested variable definitions for real AWS/Azure use cases |

---

## 🧪 How to Run Labs

Follow these steps to test any lab locally:

```bash
# Step 1 — Initialize Terraform
terraform init

# Step 2 — Review the execution plan
terraform plan -var-file="terraform.tfvars"

# Step 3 — Apply the configuration
terraform apply -var-file="terraform.tfvars"
# Type 'yes' when prompted to confirm deployment.

# Step 4 — Destroy resources after testing to avoid AWS costs
terraform destroy -var-file="terraform.tfvars"

💡 Tip: Always clean up after testing using the destroy command.
