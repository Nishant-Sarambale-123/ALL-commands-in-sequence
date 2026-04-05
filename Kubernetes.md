Here’s a **complete Terraform flow (start → end)** exactly how you use it in real DevOps projects 👇

---

# 🚀 1. Install Terraform

Download from 👉 Terraform official site

Verify:

```bash
terraform -version
```

---

# ⚙️ 2. Configure Cloud Provider (Example: AWS)

```hcl
provider "aws" {
  region = "ap-south-1"
}
```

👉 Authentication (any one):

* AWS CLI (`aws configure`)
* Access key & secret key
* IAM role (best practice)

---

# 📁 3. Create Terraform Files

Common structure:

```bash
main.tf        # resources
variables.tf   # input variables
outputs.tf     # outputs
terraform.tfvars # values
```

---

# 🧱 4. Write First Resource

Example EC2:

```hcl
resource "aws_instance" "my_ec2" {
  ami           = "ami-123456"
  instance_type = "t2.micro"
}
```

---

# 🔍 5. Initialize Terraform

```bash
terraform init
```

👉 Downloads providers & plugins

---

# 📊 6. Validate Configuration

```bash
terraform validate
```

---

# 👀 7. Preview Changes (Plan)

```bash
terraform plan
```

👉 Shows:

* What will be created
* Modified
* Destroyed

---

# 🏗️ 8. Apply (Create Infrastructure)

```bash
terraform apply
```

👉 Auto approve:

```bash
terraform apply -auto-approve
```

---

# 🔎 9. Check State

```bash
terraform show
terraform state list
```

👉 State file:

```
terraform.tfstate
```

---

# ✏️ 10. Modify Infrastructure

* Change `.tf` file
* Run again:

```bash
terraform plan
terraform apply
```

---

# ❌ 11. Destroy Infrastructure

```bash
terraform destroy
```

---

# 📦 12. Variables (Important)

```hcl
variable "instance_type" {
  default = "t2.micro"
}
```

Use:

```hcl
instance_type = var.instance_type
```

---

# 📤 13. Outputs

```hcl
output "instance_ip" {
  value = aws_instance.my_ec2.public_ip
}
```

---

# 🔐 14. Remote State (Production)

Use S3:

```hcl
terraform {
  backend "s3" {
    bucket = "my-terraform-state"
    key    = "project/terraform.tfstate"
    region = "ap-south-1"
  }
}
```

---

# 🌿 15. Workspaces

```bash
terraform workspace new dev
terraform workspace new prod
terraform workspace list
terraform workspace select dev
```

---

# 🧩 16. Modules (Reusable Code)

```hcl
module "ec2" {
  source = "./modules/ec2"
}
```

---

# 🔁 17. Import Existing Resources

```bash
terraform import aws_instance.my_ec2 i-123456
```

---

# 🔄 18. Format Code

```bash
terraform fmt
```

---

# 🔍 19. Graph (Optional)

```bash
terraform graph
```

---

# 🧠 Real DevOps Workflow (Important)

```bash
# Step 1
terraform init

# Step 2
terraform plan

# Step 3
terraform apply

# Step 4 (changes)
terraform plan
terraform apply

# Step 5 (cleanup)
terraform destroy
```

---

# 📌 Terraform Flow Summary

```
write code → init → validate → plan → apply → modify → destroy
```

---

# ⚡ Pro Tips (Interview + Real World)

* Always use **remote state (S3 + DynamoDB locking)**
* Never commit `terraform.tfstate`
* Use **modules** for reusable infra
* Use **variables & tfvars** for environments
* Prefer **IAM roles** over access keys

---

# ✅ Key Takeaway

👉 Terraform is **Infrastructure as Code (IaC)** tool used to:

* Create
* Update
* Delete infrastructure automatically

---

If you want next level:
✅ Terraform interview questions (basic → advanced)
✅ Real-world project (VPC + EC2 + ALB full setup)
✅ Comparison: Terraform vs CloudFormation

Just tell 👍
