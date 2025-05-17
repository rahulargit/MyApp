# CI/CD Deployment Assignment — MyApp & MyExpress (Windows)

## 🔧 Applications

| App        | Framework | Port  | URL                   |
|------------|-----------|-------|------------------------|
| MyApp      | Flask     | 5000  | http://localhost:5000 |
| MyExpress  | Express   | 3000  | http://localhost:3000 |

Managed by PM2, deployed via Jenkins, auto-triggered via GitHub webhook.

---

## 🚀 CI/CD with Jenkins

Each application has a Jenkins pipeline that:

- Clones the GitHub repo
- Installs required dependencies
- Restarts the app using PM2
- Gets triggered via GitHub webhook on push

---

## 🛠 Tools Used

- Python 3 (Flask)
- Node.js (Express)
- PM2 for process management
- Jenkins (local)
- GitHub for SCM

---

## ✅ Setup Summary

1. Install Python, Node.js, Git, Jenkins
2. Clone repos: `MyApp`, `MyExpress`
3. Configure Jenkins pipelines using provided `Jenkinsfile`
4. Add GitHub webhooks to trigger Jenkins on push
5. Apps accessible locally at:
   - MyApp: http://localhost:5000
   - MyExpress: http://localhost:3000

---

## 📸 Screenshots to Include

- Jenkins dashboard (build success for MyApp and MyExpress)
- `pm2 list` showing apps running
- Browser output for both apps

---

## 🔐 Optional Enhancements

- Add a `test` stage using `pytest` or `jest`
- Use Jenkins credentials for secrets
