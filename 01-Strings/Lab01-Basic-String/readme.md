# 🧩 01 – String Variable Labs

This chapter focuses on mastering **string variables** in Terraform through real examples.  
Each lab covers a practical scenario with explanation, commands, and expected outputs.

---

## 📘 Labs Summary

| Lab | Title | Description |
|-----|--------|--------------|
| **Lab 01** | Basic String Interpolation | Learn how to use `${var.name}` syntax and override defaults using `terraform.tfvars`. |
| **Lab 02** | String Concatenation & Defaults | Combine multiple string variables dynamically to create meaningful names. |
| **Lab 03** | Conditional String (Ternary Operator) | Use the `? :` operator to build environment-based outputs (e.g., prod vs dev). |

---

## ⚙️ How to Run

You can test each lab in two ways — using defaults or using the `terraform.tfvars` file.

### ▶️ Using Default Values
```bash
terraform init
terraform plan
terraform apply
