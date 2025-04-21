# Terraform AWS EC2 Ubuntu Instance with Docker

This Terraform module provisions an AWS EC2 instance using an Ubuntu AMI and installs Docker on it automatically.

> ⚠️ **Note:** This module is for educational and demonstration purposes only. It is not intended for production use.

---

## 📦 What It Does

- Launches an EC2 instance with Ubuntu
- Installs Docker on the instance via user data
- Allows specifying your own SSH key name

---

## 🚀 Usage

```hcl
provider "aws" {
  region = "us-east-1"
}

module "docker_instance" {
  source   = "github.com/erkanbarann/docker-ec2/aws"
  key_name = "firstpem"
}
