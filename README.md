# 🚀 My Linux Command Histor Save 🤖

Command History for Futher use

---


## 🚀 Code Guide

### 1. GitHub Command Line 

```bash
# පරණ Git සැකසුම් මකන්න
rm -rf .git

# අලුතින් Git එකක් ආරම්භ කරන්න
git init

# ඔබේ විස්තර ලබා දෙන්න
git config user.email "ඔබේ_EMAIL_එක"
git config user.name "erandiya"

# රහස්‍ය දත්ත සහ විශාල ෆයිල් ඉවත් කිරීමට .gitignore තහවුරු කරගන්න
nano .gitignore

# ෆයිල් එකතු කරන්න
git add .

# Commit එකක් කරන්න
git commit -m "Final cleanup and merged system"

# GitHub එක සම්බන්ධ කරන්න
git branch -M main
git remote add origin https://github.com/erandiya/Telegram-WhatsApp-Forwarder.git

# නෝර්මල් Push කරන්න
git push origin main 

# බලහත්කාරයෙන් Push කරන්න
git push origin main --force

# ෆයිල් අයින් කරන්න
git rm README.md.save* index.js.bak sync.php.bak

```

---

### 2. 'pm2' Command Line 

```bash
sudo add-apt-repository ppa:ondrej/php -y
sudo apt update
sudo apt install -y php8.2-cli php8.2-curl php8.2-mbstring php8.2-xml php8.2-zip php8.2-gmp php8.2-ffi php8.2-common
# Enable FFI in PHP
echo "ffi.enable=true" | sudo tee -a /etc/php/8.2/cli/php.ini 
```

---

### 👨‍💻 Author
Developed by **[Erandiya Sumanaweera.](https://fb.com/erandiya)**

---