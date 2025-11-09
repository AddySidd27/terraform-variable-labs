🧩 Lab 01 — Basic String Interpolation
🎯 Goal

Understand how to use a variable inside a string using ${} interpolation.

📄 variables.tf
variable "environment" {
  description = "Environment name (dev, test, or prod)"
  type        = string
  default     = "dev"
}

📄 main.tf
output "env_message" {
  value = "This is the ${var.environment} environment"
}

📄 terraform.tfvars
environment = "production"

▶️ How to Run
Option 1 — Default Run (uses default = "dev")
terraform init
terraform plan
terraform apply

✅ Expected Output
env_message = "This is the dev environment"

Option 2 — Using terraform.tfvars
terraform init
terraform plan -var-file="terraform.tfvars"
terraform apply -var-file="terraform.tfvars"

✅ Expected Output
env_message = "This is the production environment"

💬 Explanation

${var.environment} injects the variable value into the string dynamically.

If you don’t use -var-file, Terraform picks the default "dev".

If you use terraform.tfvars, it overrides the default with "production".

This pattern is useful when switching between dev/test/prod environments.

🧾 Summary
Concept	Description
Variable Interpolation	${} syntax inserts variable values into strings
Default Value	Terraform uses the default field if no external value is passed
.tfvars Override	The value from terraform.tfvars takes precedence
🧑‍💻 Example Workflow
# Default run (uses 'dev')
terraform apply

# Run with .tfvars (uses 'production')
terraform apply -var-file="terraform.tfvars"

# Clean up
terraform destroy -var-file="terraform.tfvars"

🏁 Lab Outcome

You now understand how to:

Use string interpolation in Terraform

Manage default vs external variable values

Apply and destroy configurations cleanly