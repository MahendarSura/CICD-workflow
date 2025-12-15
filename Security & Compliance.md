# 6️⃣ Security & Compliance – Simple Telugu-Medium Style

---

## 6.1 Secrets Management

### Emti (What):
Passwords, API keys, tokens ni **code lo hardcode cheyakunda safe ga store cheyadam**.

### Enduku Use Cheyali (Why):
- Code leak ayithe secrets safe undali  
- Unauthorized access prevent cheyali  

### Ela Use Chestharu (How):
- GitHub Secrets / HashiCorp Vault / AWS Secrets Manager lo store  
- Pipeline runtime lo fetch → use cheyadam  
- Code lo hardcoding avoid cheyadam  

### Real-Time Daily CI/CD Workflow – Secrets
- **What:** Secrets secure ga store & fetch cheyadam  
- **Why:** Security maintain, leaks avoid  
- **When:** Every pipeline run  
- **Where:** CI/CD system, production  
- **How:** Pipeline fetch → deploy → logs maintain  

---

## 6.2 Vulnerability Checks

### Emti (What):
App / infra lo **security holes** unnaya ani automatic scan cheyadam  

### Enduku Use Cheyali (Why):
- Vulnerabilities detect cheyadam  
- Production security maintain cheyadam  

### Ela Use Chestharu (How):
- Dependabot, Snyk, Trivy tools integrate  
- Pipeline run ayyaka scan  
- Issues detect ayithe fail / warn generate  
- DevOps fix → redeploy  

### Real-Time Daily CI/CD Workflow – Vulnerability
- **What:** Automatic vulnerability scan  
- **Why:** Security risk thaggutundi  
- **When:** Every pipeline run  
- **Where:** CI/CD system  
- **How:** Pipeline scan → alert → fix → redeploy  

---

## 6.3 Policy Enforcement

### Emti (What):
Rules follow cheyithe **deploy allow cheyadam**  

### Enduku Use Cheyali (Why):
- Unauthorized / unsafe changes prevent  
- Compliance maintain  

### Ela Use Chestharu (How):
- PR raise → reviewer approval  
- Branch protection rules  
- Pipeline verify cheyadam → allow / block deploy  

### Real-Time Daily CI/CD Workflow – Policy Enforcement
- **What:** Deploy only if rules satisfied  
- **Why:** Compliance & safety  
- **When:** Every PR / deploy  
- **Where:** Git repository, CI/CD system  
- **How:** Pipeline verify → approve → deploy  

---

## 6.4 Real-Time Daily CI/CD Workflow – Security Summary

- **What:** Secure deploy with secrets & scans  
- **Why:** Hack, leaks & vulnerabilities avoid  
- **When:** Every pipeline run  
- **Where:** CI/CD system, production servers  
- **How:**  
  1. Secret fetch & use  
  2. Vulnerability scan  
  3. Policy enforcement  
  4. Deploy only if all checks pass  
  5. Logs maintain for audit
