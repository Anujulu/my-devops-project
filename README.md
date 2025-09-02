
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

## **3. Build the Node.js Web App**
**Initialize Project**

    ```bash

        npm init -y

    ```
 This creates a package.json. Update it as follows:
    ```json
            {
        "name": "my-devops-project",
        "version": "1.0.0",
        "description": "DevOps learning project with Node.js",
        "main": "app.js",
        "scripts": {
            "start": "node app.js",
            "test": "jest",
            "dev": "node app.js",
            "lint": "eslint ."
        },
        "keywords": ["devops", "nodejs", "docker"],
        "author": "Your Name",
        "license": "MIT",
        "engines": { "node": ">=18.0.0" },
        "devDependencies": {
            "jest": "^29.7.0",
            "eslint": "^8.57.0",
            "supertest": "^7.1.4"
        }
        }

    ```
**Create Application File**

    ```bash

        touch app.js

    ```
   