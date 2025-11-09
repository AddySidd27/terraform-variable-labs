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
📄 main.tf
hcl
Copy code
output "env_message" {
  value = "This is the ${var.environment} environment"
}
📄 terraform.tfvars
hcl
Copy code
environment = "production"
▶️ How to Run
Option 1 — Default Run (uses default = "dev")
bash
Copy code
terraform init  
terraform plan  
terraform apply
Expected Output

ini
Copy code
env_message = "This is the dev environment"
Option 2 — Using terraform.tfvars (uses "production")
bash
Copy code
terraform init  
terraform plan -var-file="terraform.tfvars"  
terraform apply -var-file="terraform.tfvars"
Expected Output

ini
Copy code
env_message = "This is the production environment"
💬 Explanation
${var.environment} injects the variable value into the string dynamically.

If you don’t use -var-file, Terraform uses the default "dev".

If you provide terraform.tfvars, it overrides the default with "production".

Helps manage multiple environments like dev/test/prod easily.

🧾 Summary
Concept	Description
Variable Interpolation	${} inserts variable values into strings
Default Value	Terraform uses default if no external value is passed
tfvars Override	Values in .tfvars file override defaults

🧑‍💻 Example Workflow
bash
Copy code
# Default run (uses 'dev')  
terraform apply  

# Run with .tfvars (uses 'production')  
terraform apply -var-file="terraform.tfvars"  

# Clean up resources  
terraform destroy -var-file="terraform.tfvars"
🏁 Lab Outcome
You learned how to:

Use string interpolation in Terraform

Work with default and external variables

Apply and destroy infrastructure cleanly

🔗 Next Lab
➡️ Lab 02 — String Concatenation and Dynamic Messages
