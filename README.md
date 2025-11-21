# CryptoPulse-app – End-to-End AWS + GitHub OIDC DevOps Project

CryptoPulse is a production-ready static crypto insights application built with an enterprise-grade AWS architecture, full CI/CD automation using GitHub Actions, and secure deployments using OIDC (no secret keys).

This project demonstrates real-world DevOps + Cloud Architecture capabilities: Infrastructure-as-Code, automated deployments, monitoring, secure IAM roles, and fast global delivery.

🌐 **Live Demo**

CryptoPulse-app Live App (GitHub Pages)
https://cloud-architect-emma.github.io/cryptopulse-app/

Available for cloning
Explore, fork, improve the UI
Ideal for DevOps/Cloud portfolio demonstration

##  Architecture Overview

This project uses a full production-like AWS stack:

AWS S3 → static website hosting

AWS CloudFront → CDN distribution (used originally)

AWS IAM + OIDC → secure role-based GitHub authentication

AWS CloudWatch → logging + metrics + alarms

GitHub Actions CI/CD → automated build, deployment & invalidation

Terraform → Infrastructure as Code (IaC) for AWS resources

## Architecture Diagram:
![Architecture Diagram](screenshots/OIDC%20App.gif)

📁 For more screenshots, open the screenshots folder in the repository.

## CI/CD Pipeline (AWS OIDC — No Access Keys Required)

This project uses GitHub Actions + AWS IAM OIDC to deploy securely:

No long-lived AWS IAM secrets

GitHub automatically requests short-lived JWT tokens

Pipeline assumes an IAM role with trust relationship

S3 sync + CloudFront invalidation happens automatically

## Workflow Includes:

Code validation

Upload to S3

Cache invalidation

Error handling & rollback safety

You can request the workflow YAML and Terraform snippets inside the repo or read them directly under:

.github/workflows/deploy.yml  
terraform/

## Tech Stack
```
Frontend

HTML

CSS

JavaScript

AWS

S3

CloudFront

IAM

CloudWatch

SNS (for optional alerts)

Route 53 (health checks)
```

## DevOps
```
GitHub Actions

OIDC Authentication
```
## Terraform
📁 Project Structure
.
├── index.html
├── assets/
├── styles/
├── scripts/
├── terraform/
├── .github/
│   └── workflows/
│       └── deploy.yml
└── screenshots/
        ├── OIDC App.gif
        └── *.png (other images)

## How to Deploy This Yourself
Clone the Repository
git clone https://github.com/Cloud-Architect-Emma/cryptopulse-app.git
cd cryptopulse-app

Modify the UI (optional)

The app is pure HTML/CSS/JS — very easy to customize.

Deploy Infra with Terraform
cd terraform
terraform init
terraform apply

Push Code → Automatic Deployment

GitHub Actions + OIDC will deploy automatically to your S3 bucket.

## Monitoring & Observability

CloudWatch Metrics

CloudWatch Logs

SNS Notifications

Health Checks via Route 53

Error rate tracking

Latency metrics

## Contributing

Want to improve the app UI, add animations, or enhance the pipeline?
Feel free to:

Fork the repo

Open a PR

Add new features

**Author**

Emmanuela (Cloud Architect & DevOps Engineer)
GitHub: https://github.com/Cloud-Architect-Emma

**Support the Project**

If you find this helpful, kindly ⭐ star the repository.

It helps visibility and supports the open-source journey.
