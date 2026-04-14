# 🚀 Static Website Deployment using AWS CI/CD

## 📌 Overview
This project deploys a static website using AWS CI/CD.

## 🔄 Flow
GitHub → CodePipeline → CodeBuild → S3 → Live Website

## 🛠️ Tech Used
- HTML, CSS, JS
- AWS S3
- CodePipeline
- CodeBuild

## ⚙️ Steps

1. Create S3 bucket → `my-static-site-000`  
2. Enable Static Website Hosting → index.html  
3. Add bucket policy (public access)  
4. Add files in GitHub:
   - index.html  
   - buildspec.yml  

5. buildspec.yml:
```yaml
version: 0.2
phases:
  build:
    commands:
      - echo "Build phase"
artifacts:
  files:
    - '**/*'
