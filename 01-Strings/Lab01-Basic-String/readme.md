## 🧩 Lab 01 — Basic String Interpolation  

### 🎯 Goal  
Understand how to use a variable inside a string using `${}` interpolation.  

---

### 📄 variables.tf  
```hcl
variable "environment" {
  description = "Environment name (dev, test, or prod)"
  type        = string
  default     = "dev"
}
```

---

### 📄 main.tf  
```hcl
output "env_message" {
  value = "This is the ${var.environment} environment"
}
```

---

### 📄 terraform.tfvars  
```hcl
environment = "production"
▶️ How to Run
Option 1 — Default Run (uses default = "dev")
bash
Copy code
terraform init  
terraform plan  
=======
```

---

### ▶️ How to Run  

#### Option 1 — Default run (uses default = "dev")
```bash
terraform init
terraform plan
>>>>>>> 3e4b26f (Added Lab01 Basic String Interpolation with formatted markdown)
terraform apply
```

**Expected Output**
```ini
env_message = "This is the dev environment"
Option 2 — Using terraform.tfvars (uses "production")
bash
Copy code
terraform init  
terraform plan -var-file="terraform.tfvars"  
=======
```

---

#### Option 2 — Run using terraform.tfvars (uses "production")
```bash
terraform init
terraform plan -var-file="terraform.tfvars"
>>>>>>> 3e4b26f (Added Lab01 Basic String Interpolation with formatted markdown)
terraform apply -var-file="terraform.tfvars"
```

**Expected Output**
```ini
env_message = "This is the production environment"
```

---

### 💬 Explanation  
`${var.environment}` dynamically injects the variable value into the string.  

Helps manage multiple environments like dev/test/prod easily.
=======
If you don’t use `-var-file`, Terraform picks the default value `"dev"`.  
>>>>>>> 3e4b26f (Added Lab01 Basic String Interpolation with formatted markdown)

If you use `terraform.tfvars`, it overrides the default with `"production"`.  

🧑‍💻 Example Workflow
bash
Copy code
# Default run (uses 'dev')  
terraform apply  

# Run with .tfvars (uses 'production')  
terraform apply -var-file="terraform.tfvars"  
=======
This helps manage multiple environments like dev/test/prod easily.  

---

### 🧾 Summary  
| Concept | Description |
|----------|--------------|
| Variable Interpolation | `${}` inserts variable values into strings |
| Default Value | Terraform uses the default if no external value is passed |
| tfvars Override | `.tfvars` file overrides defaults |

---

### 🧑‍💻 Example Workflow  
```bash
# Default run (uses "dev")
terraform apply

# Run with .tfvars (uses "production")
terraform apply -var-file="terraform.tfvars"
>>>>>>> 3e4b26f (Added Lab01 Basic String Interpolation with formatted markdown)

# Clean up resources  
terraform destroy -var-file="terraform.tfvars"
```

---

### 🏁 Lab Outcome  
You have learned how to:

Apply and destroy infrastructure cleanly

🔗 Next Lab
➡️ Lab 02 — String Concatenation and Dynamic Messages
