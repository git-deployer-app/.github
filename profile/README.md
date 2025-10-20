# GitDeployer 🚀

**GitDeployer** is a lightweight, script-based deployment tool that automates your application deployment process directly from your Git repository. It's designed to be simple, customizable, and technology-agnostic.

Stop manual deployments. Start deploying with a single git push.

[![GitHub License](https://img.shields.io/github/license/git-deployer-app/gitdeployer)](https://github.com/git-deployer-app/gitdeployer/blob/main/LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/git-deployer-app/gitdeployer/pulls)

---

## ✨ Features

*   **Simple Setup**: Get started in minutes with a single configuration file.
*   **Technology Agnostic**: Deploy PHP, Node.js, Python, Go, or static sites. It's all about the scripts.
*   **Webhook Support**: Automatically trigger deployments on `git push` using GitHub, GitLab, or Gitea webhooks.
*   **Pre & Post-Deployment Hooks**: Run custom scripts before or after deployment (e.g., install dependencies, run tests, clear cache).
*   **Secure by Design**: Uses secret tokens for webhook authentication and runs with strict permissions.
*   **Logging**: Built-in logging for debugging your deployment process.

## 🏗️ How It Works

1.  You push your code to the `main` branch (or any branch you configure).
2.  Your Git hosting service sends a POST request (webhook) to your server.
3.  The GitDeployer webhook listener receives the request, verifies it, and triggers the deployment script.
4.  The deployment script pulls the latest code, runs your build steps, and restarts your application.

## 📦 Quick Start

### 1. Clone and Setup on Your Server

SSH into your server and clone this repository.

```bash
git clone https://github.com/git-deployer-app/gitdeployer.git
cd gitdeployer
