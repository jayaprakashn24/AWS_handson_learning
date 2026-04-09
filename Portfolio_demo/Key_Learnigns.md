🚀 **Deploying a Static Website Using Apache/Nginx on Ubuntu (AWS EC2)**

---

## 🖥️ Step 1: Launch EC2 Instance

* **AMI**: Ubuntu Server 24.04 LTS
* **Instance Type**: t3.micro (Free Tier eligible)
* **Architecture**: 64-bit (x86)
* **Storage**: SSD (EBS)
* **Username**: `ubuntu`

---

## 🔐 Step 2: Connect to Your Server

```bash
ssh -i your-key.pem ubuntu@your-public-ip
```

---

## 🔄 Step 3: Update Packages

```bash
sudo apt update
```

---

## 🌐 Step 4: Install Web Server (Nginx)

```bash
sudo apt install nginx -y
```

---

## ▶️ Step 5: Start & Enable Nginx

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```

---

## 📊 Step 6: Check Server Status

```bash
sudo systemctl status nginx
```

---

## 📁 Step 7: Deploy Your Static Website

Replace default HTML files with your own:

```bash
cd /var/www/html
sudo rm index.nginx-debian.html
sudo nano index.html
```

👉 Paste your HTML code and save.

---

## 🌍 Step 8: Access Website

Open your browser:

```
http://your-public-ip
```

---

## 📦 Step 9: Upload Project to GitHub

### Initialize Git

```bash
git init
git add .
git commit -m "Initial commit - Static website deployment"
```

### Create Repository on GitHub and Push

```bash
git remote add origin https://github.com/your-username/your-repo.git
git branch -M main
git push -u origin main
```

---

## ✅ Project Structure Example

```
static-website/
│── index.html
│── style.css
│── script.js
```

---

## 💡 Key Learnings

* Launching EC2 instances
* Connecting via SSH
* Installing and managing Nginx
* Hosting static websites
* Version control with Git & GitHub

---

## 🔥 Pro Tip

If your site doesn’t load:

* Check **Security Group** → Allow HTTP (Port 80)
* Verify Nginx is running

---


