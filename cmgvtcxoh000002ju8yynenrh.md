---
title: "Day 1: Terraform Associate Journey"
seoTitle: "Starting the Terraform Associate Journey"
seoDescription: "Start my Terraform journey by building a complete AWS VPC, focusing on hands-on implementation and Infrastructure as Code"
datePublished: Sat Oct 18 2025 05:04:51 GMT+0000 (Coordinated Universal Time)
cuid: cmgvtcxoh000002ju8yynenrh
slug: day-1-terraform-associate-journey
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1760763604323/fff96d20-c025-4fcf-b1df-226f8dcb8123.png
tags: aws, cloud-computing, devops, terraform, certification, vpc, devops-journey

---

Today marks **Day 1** of my Terraform Certified Associate preparation.  
Instead of just reading theory, I jumped straight into **hands-on implementation** by building a complete **AWS VPC architecture** using Terraform.

---

# 🧩 What I Built

I designed and deployed a **highly available VPC architecture** spread across **three Availability Zones** (`us-east-1a`, `us-east-1b`, `us-east-1c`).  
Here’s what the setup includes:

* 🏗️ **1 VPC** — to hold all networking resources
    
* 🌐 **3 Public Subnets** — one in each Availability Zone
    
* 🔒 **3 Private Subnets** — for backend resources
    
* 🚪 **Internet Gateway (IGW)** — allows internet access to public subnets
    
* 🌉 **NAT Gateway** — placed in one public subnet to give private subnets secure outbound internet access
    
* 🗺️ **Public & Private Route Tables** — to manage routing for respective subnets
    

This architecture ensures **fault tolerance, scalability, and security**, all powered by Infrastructure as Code (IaC) using Terraform.

---

# **🧠 Understanding the Architecture**

The logic is simple yet powerful:

* **Public Subnets** connect directly to the **Internet Gateway** — perfect for hosting web servers.
    
* **Private Subnets** remain isolated — ideal for databases or internal apps — but can still access the internet via the **NAT Gateway** for updates or dependencies.
    
* **Route Tables** define these paths, ensuring every subnet knows how to communicate securely.
    

In short — this is the same kind of network architecture real production environments use.

---

# 💻 My Terraform Implementation Experience

As I wrote the Terraform configuration, I started appreciating how cleanly **Terraform turns cloud infrastructure into code**.  
A few things that stood out today:

* ✅ Using **variables** for CIDR blocks, region, and subnet counts made the code reusable.
    
* ✅ **Outputs** helped me confirm VPC IDs and subnet IDs after `apply`.
    
* ✅ **Modules** make large projects cleaner — I’ll refactor into modules soon.
    
* ✅ I learned how **state files** are the brain of Terraform — tracking what’s created, changed, or destroyed.
    

At first, I faced small hiccups aligning subnet CIDRs and AZ mappings, but once configured, the entire setup launched flawlessly with one command.

---

# ⚙️ Important Terraform Commands I Used

Here’s a quick list of the commands that became my daily essentials today:

| Command | Description |
| --- | --- |
| `terraform init` | Initializes Terraform — downloads the provider plugins (in my case, AWS). |
| `terraform fmt` | Formats your Terraform code for better readability. |
| `terraform validate` | Checks if your configuration files are syntactically correct. |
| `terraform plan` | Shows what Terraform *will* create, modify, or destroy before applying. |
| `terraform apply` | Executes the plan — actually provisions your infrastructure on AWS. |
| `terraform show` | Displays the current state or details of deployed resources. |
| `terraform state list` | Lists all resources tracked by Terraform state. |
| `terraform destroy` | Tears down everything Terraform created — used carefully! |
| `terraform output` | Prints the values of declared outputs (e.g., VPC ID, Subnet IDs). |

👉 **Pro Tip:** Always run `terraform plan` before `terraform apply`. It’s like previewing your changes before pressing *Deploy*.

---

# 📘 What I Learned Today

1. **Terraform is declarative** — you define *what you want*, Terraform figures out *how to get there*.
    
2. **Infrastructure as Code (IaC)** brings version control and repeatability to cloud setups.
    
3. **State management** and **backend storage** are key concepts I’ll explore more in the coming days.
    
4. Knowing **AWS networking basics** (VPCs, subnets, NAT, IGW, routes) is essential before diving deep into Terraform.
    

---

# 🧭 What’s Next (Day 2 Plan)

Tomorrow, I’ll focus on:

* Terraform **providers and modules**
    
* Launching **EC2 instances** inside public and private subnets
    
* Exploring **remote backend configurations** and `terraform.tfstate` best practices
    

---

# Final Thoughts

Day 1 gave me a solid start — not just theory, but actual deployment.  
Seeing my AWS VPC come alive through Terraform commands felt empowering. The beauty of Terraform lies in how **a few lines of code can build an entire cloud architecture**.

It’s clear now: mastering Terraform isn’t just about memorizing commands — it’s about understanding how code translates into real, scalable infrastructure.

---

---