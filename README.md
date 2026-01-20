# 🚀 CI/CD on cPanel using SCP

Automated CI/CD pipeline that deploys projects from **GitHub** to a **cPanel hosting account** using **SCP (Secure Copy Protocol)**.  
This setup is ideal for shared hosting environments where traditional DevOps tooling (Docker, K8s, etc.) is not available.

---

## ✨ Features

- Continuous Deployment on every push
- Automates file transfer using SCP
- Uses GitHub Actions
- Works with PHP, static sites, and simple web apps
- Secure SSH-based deployment
- Minimal configuration required

---

## 📦 How It Works

1. Push code to `main` branch
2. GitHub Actions pipeline is triggered
3. Files are copied to the server via SCP
4. Website updates automatically — no manual FTP required

---

## 🛠 Requirements

- cPanel account with **SSH enabled**
- SSH private/public keys
- GitHub repository
- Deployment directory (e.g. `public_html/`)

---

## 🔐 GitHub Secrets Setup

Add the following secrets in:

> `Settings → Secrets and Variables → Actions`

| Secret Name       | Description |
|------------------|-------------|
| `SSH_HOST`        | cPanel server hostname |
| `SSH_PORT`        | SSH port (default: 22) |
| `SSH_USER`        | cPanel username |
| `SSH_PRIVATE_KEY` | SSH private key |
| `DEPLOY_PATH`     | Deployment path (e.g. `/home/user/public_html/`) |

---

## 📁 Workflow File Example

Place this in:

