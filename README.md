# 📦 Project: EC2 Instance Launch with Enforced Tagging Policy

---

## 📌 Objective  
This project demonstrates how to enforce mandatory tagging on EC2 instances using AWS IAM policies to ensure proper cost tracking, governance, and accountability.

---

## 🏗️ Architecture Diagram  

```
User
↓
AWS Console / CLI
↓
IAM Policy (Tag Enforcement)
↓
EC2 Launch Request
↓
✔ Allowed (if tags correct)
❌ Denied (if tags missing/incorrect)
```

---

## ✅ Required Tags  

The following tags must be provided during EC2 launch:

| Tag Key | Example Value |
|--------|--------------|
| Name | Pooja |
| emailID | pooja@example.com |
| phoneNo | 9846447366 |
| Place | Pune |

---

## 🔐 Tag Policy Implementation (IAM Policy)  

An IAM policy was created to deny EC2 instance creation if required tags are missing or incorrect.

### 🔧 Policy Logic  
- Deny if required tags are missing  
- Deny if `Place` is not equal to `Pune`  

### 📜 IAM Policy JSON  
*(Add your IAM policy JSON here)*

---

## 🖥️ EC2 Launch Process (With Tags)  

### Steps:
1. Go to AWS Console → EC2 → Launch Instance  
2. In **Name and Tags** section, add all required tags:
   - Name = `<your-name>`  
   - emailID = `<your-email>`  
   - phoneNo = `<your-phoneNo>`  
   - Place = `Pune`  
3. Select AMI (Amazon Linux)  
4. Choose instance type (t3.micro)  
5. Create/select key pair  
6. Configure security group  
7. Click **Launch Instance**  

### ✅ Result:
Instance launched successfully because all required tags were present.

---

## ❌ EC2 Launch Without Tags (Failure Case)  

### Test Scenarios:
1. Missing tags  
2. Incorrect tag value (`Place ≠ Pune`)  

### ❌ Result:
- Instance launch failed  
- Error message displayed  

---

## 📸 Screenshots  

1. IAM Policy Creation  
2. EC2 Instance Running (State = running)  
3. Tags tab showing all 4 tags  
4. Error screenshot (without tags)  

---

## 🧾 Step-by-Step Guide  

### 🔹 1. Apply Tags While Launching EC2 (Console)

1. Go to AWS Console → EC2  
2. Click **Launch Instance**  
3. In **Name and Tags** section:
   - Click **Add additional tags**  
   - Add:
     - Name = Pooja  
     - emailID = poojadange1501@gmail.com  
     - phoneNo = 9322583323  
     - Place = Pune  
4. Complete remaining steps  
5. Click **Launch Instance**  

---

### 🔹 2. Enforce Tag Policy (IAM Console)

1. Go to IAM → Policies  
2. Click **Create Policy**  
3. Select **JSON tab**  
4. Paste IAM policy  
5. Click **Next** → Name policy  
6. Click **Create Policy**  
7. Attach policy to IAM User  

---

## 🔍 Observations  
- IAM policy successfully enforced tagging  
- EC2 instance creation is blocked if tags are missing  
- Helps in cost allocation and governance  

---

## 🎯 Conclusion  
This project demonstrates how AWS IAM policies can be used to enforce mandatory tagging on EC2 instances. This ensures better resource management, cost tracking, and organizational compliance.

---

## 👩‍💻 Author  

**Pooja Dange**  
Cloud & DevOps Learner  

📧 Email: poojadange1501@gmail.com  
🔗 LinkedIn: https://www.linkedin.com/in/pooja-dange-0270072b3  
💻 GitHub: https://github.com/your-username  

---
