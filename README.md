# my-devops-project
# My DevOps Project – Node.js, Docker, CI/CD, and Kubernetes

This project demonstrates how to build a modern Node.js web application, containerize it with Docker, set up CI/CD with GitHub Actions, and deploy to staging and production using Kubernetes.

---

## **1. Prerequisites**

Install these tools before starting:

### Node.js (v18 or higher)
- Download LTS (20.x as of 2025): [https://nodejs.org/](https://nodejs.org/)
- Verify installation:
  ```bash
  node --version    # Should show v18.x+ or v20.x+
  npm --version     # Should show 9.x+ or 10.x+
  ```

### Git

- Download: https://git-scm.com/downloads

- Verify installation:
```bash
  git --version      # Should show 2.34+ 

``` 

### Docker Desktop

- Download: https://www.docker.com/products/docker-desktop/

- Verify installation:

```bash
 docker --version          # Should show 24.x+
 docker-compose --version
 
```

### GitHub Account

- Sign up at: https://github.com

### Code Editor (Optional)

- [Visual Studio Code](https://code.visualstudio.com/?utm_source=chatgpt.com)
 recommended
 ---

## **2. Project Setup**
**Configure Git**

```bash

  git config --global user.name "Your Name"
  git config --global user.email "you@example.com"
  git config --global init.defaultBranch main

```

**Create Project Folder**
```bash
  mkdir my-devops-project
  cd my-devops-project
  git init

```