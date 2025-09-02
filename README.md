
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
   
Copy the [app.js](https://chatgpt.com/c/68b7466a-326c-8322-90f2-0a29af917fcf#full-appjs-code) code
 into this file.   

 **Install Dependencies**

    ```bash
        npm install --save-dev jest eslint supertest
        npm install

    ```
## **4. Testing Setup**
**Create Test Folder and File**

    ```bash
        mkdir tests
        touch tests/app.test.js

    ```
Copy the [test code](https://chatgpt.com/c/68b7466a-326c-8322-90f2-0a29af917fcf#test-code)
 into this file.    
 **Create Jest Config**

     ```bash

         touch jest.config.js

    ```

    ```js

        module.exports = {
        testEnvironment: 'node',
        collectCoverage: true,
        coverageDirectory: 'coverage',
        testMatch: ['**/tests/**/*.test.js'],
        verbose: true
    };

    ```

## **5. CI/CD with GitHub Actions**

Create workflow folder and file:   
    ```bash

        mkdir -p .github/workflows
        touch .github/workflows/ci.yml

    ```   
Copy the [pipeline code](https://chatgpt.com/c/68b7466a-326c-8322-90f2-0a29af917fcf#cicd-pipeline-code)
 into this file  

## **6. Docker Configuration**

**Create Dockerfile**

    ```bash
        touch Dockerfile

    ```

Copy the [Dockerfile code](https://chatgpt.com/c/68b7466a-326c-8322-90f2-0a29af917fcf#dockerfile-code)
 into this file.

 **Create .dockerignore**

 What this file does: Tells Docker which files to ignore when building the container image (similar to .gitignore).

How to create the file:

     ```bash
         touch .dockerignore

    ```
 Copy this content into .dockerignore:

    (node_modules npm-debug.log* .git .github .env .env.local .env.*.local logs *.log coverage .nyc_output .vscode .idea *.swp *.swo .DS_Store Thumbs.db README.md tests/ jest.config.js .eslintrc*)

Create .gitignore
    What this file does: Tells Git which files to ignore and not track in version control (like temporary files, dependencies, etc.).

How to create the file:

    ```bash
        touch .gitignore
    ```

 Copy this content into .gitignore:

 (Dependencies node_modules/ npm-debug.log*   *.pid *.seed *.pid.lock   coverage/ .nyc_output   .env .env.local .env.*.local   logs *.log   .vscode/ .idea/ *.swp *.swo   .DS_Store Thumbs.db)
