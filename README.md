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
git config user.email "gayan@gmail.com"
git config user.name "gayan"

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

# 🛠️ PM2 Command Cheat Sheet (වැදගත්ම විධානයන්)

ඔබේ VPS එකේ කටයුතු පහසු කර ගැනීම සඳහා **PM2 (Process Manager 2)** හි භාවිතා වන වැදගත්ම කමාන්ඩ් (Commands) ටික මෙන්න. මෙය ඔබට ඕනෑම වෙලාවක බලා ගැනීමට "Cheat Sheet" එකක් ලෙස පාවිච්චි කළ හැක.

---

### 🚀 1. වැඩසටහන් ආරම්භ කිරීම (Starting)

*   **අලුතින් ස්ක්‍රිප්ට් එකක් නමක් සහිතව ආරම්භ කිරීමට:**
    ```bash
    pm2 start index.js --name "whatsapp-api"
    ```
*   **සර්වර් එකේ සියලුම CPU Cores භාවිතා කරමින් (Cluster mode) රන් කිරීමට:**
    ```bash
    pm2 start index.js -i max
    ```

---

### 📊 2. තත්ත්වය පරීක්ෂා කිරීම (Monitoring)

*   **දැනට රන් වන වැඩසටහන් ලැයිස්තුව සහ ඒවායේ තත්ත්වය (Online/Stopped) බැලීමට:**
    ```bash
    pm2 status
    ```
    *(නැතහොත් `pm2 list` භාවිතා කළ හැක)*

*   **සියලුම වැඩසටහන් වල සජීවී ලොග් (Messages/Errors) බැලීමට:**
    ```bash
    pm2 logs
    ```
*   **එක් විශේෂිත වැඩසටහනක ලොග් පමණක් බැලීමට:**
    ```bash
    pm2 logs whatsapp-api
    ```
*   **සර්වර් එකේ CPU සහ RAM භාවිතය Dashboard එකක් ලෙස බැලීමට:**
    ```bash
    pm2 monit
    ```

---

### 🔄 3. පාලනය කිරීම (Control)

*   **දැනට රන් වන සියලුම වැඩසටහන් නැවැත්වීමට:**
    ```bash
    pm2 stop all
    ```
*   **සියලුම වැඩසටහන් නැවත පණ ගැන්වීමට (Restart):**
    ```bash
    pm2 restart all
    ```
*   **වැඩසටහන සම්පූර්ණයෙන්ම නතර නොකර අලුත් කේතයන් ලබා ගැනීමට (Zero-downtime):**
    ```bash
    pm2 reload all
    ```
*   **ලැයිස්තුවෙන් සියලුම වැඩසටහන් සම්පූර්ණයෙන්ම ඉවත් කිරීමට:**
    ```bash
    pm2 delete all
    ```

---

### 💾 4. සර්වර් එක Reboot වුවහොත් (Persistence)

*   **දැනට රන් වන ලිස්ට් එක සේව් කිරීමට:**
    *(සර්වර් එක Restart වුවහොත් මේ ලිස්ට් එකම නැවත පණ ගැන්වේ)*
    ```bash
    pm2 save
    ```
*   **සර්වර් එක ඔන් වන විටම PM2 ස්වයංක්‍රීයව ආරම්භ වීමට අවශ්‍ය කේතය ලබා ගැනීමට:**
    ```bash
    pm2 startup
    ```
    *(සටහන: මෙය ගැසූ පසු ටර්මිනල් එකේ ලැබෙන පේළිය කොපි කර පේස්ට් කර රන් කරන්න)*

---

### 🧹 5. නඩත්තුව (Maintenance)

*   **පරණ Log ෆයිල්ස් මකා දමා Disk Space නිදහස් කිරීමට (ඉතා වැදගත්):**
    ```bash
    pm2 flush
    ```
*   **PM2 මෘදුකාංගය අලුත් (Update) කිරීමට:**
    ```bash
    pm2 update
    ```

---

### 💡 නිතරම භාවිතා වන පේළිය (The Combo)

ඔබ කේතයේ (Code) වෙනසක් කළ පසු පද්ධතිය සම්පූර්ණයෙන් පිරිසිදු කර නැවත පණ ගැන්වීමට මෙය භාවිතා කරන්න:

```bash
pm2 flush && pm2 restart all && pm2 status
```

---

### 👨‍💻 Author
Developed by **[Erandiya Sumanaweera.](https://fb.com/erandiya)**

---