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

# ගිට් ෙටා්කන් Cache temporarily (restart/logout වෙනකම් හෝ timeout එකකට)
git config --global credential.helper cache

# Custom timeout (e.g. 1 hour = 3600 sec):
git config --global credential.helper 'cache --timeout=3600'

# Save permanently in plaintext file (~/.git-credentials)
git config --global credential.helper store
cat ~/.git-credentials
# https://USERNAME:TOKEN@github.com         //Example format

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

# 🛠️ VPS Management & Maintenance Guide (පාලන සහ නඩත්තු අත්පොත)

මෙම ලේඛනය මගින් පද්ධතියේ සේවාවන් පාලනය කරන ආකාරය සහ VPS එකේ නඩත්තු කටයුතු සිදුකරන ආකාරය පැහැදිලි කරයි.

---

## 🚀 1. PM2 Process Manager (සේවාවන් පාලනය)

PM2 භාවිතා කරන්නේ WhatsApp API එක පසුබිමින් දිගටම ක්‍රියාත්මක කර තැබීමටයි.

### ✅ ආරම්භ කිරීම (Starting)
*   **අලුතින් සේවාවක් ආරම්භ කිරීමට:**
    ```bash
    pm2 start index.js --name "whatsapp-api"
    ```
*   **සර්වර් එකේ උපරිම හැකියාව භාවිතා කරමින් රන් කිරීමට:**
    ```bash
    pm2 start index.js -i max
    ```

### 📊 පරීක්ෂා කිරීම (Monitoring)
*   **දැනට රන් වන සේවාවන් ලැයිස්තුව බැලීමට:**
    ```bash
    pm2 status
    ```
*   **සජීවී ලොග් (Live Logs) පරීක්ෂා කිරීමට:**
    ```bash
    pm2 logs whatsapp-api
    ```
*   **CPU සහ RAM භාවිතය Dashboard එකක් ලෙස බැලීමට:**
    ```bash
    pm2 monit
    ```

### 🔄 පාලනය (Control)
*   **සේවාවන් නැවැත්වීමට (Stop):**
    ```bash
    pm2 stop all
    ```
*   **සේවාවන් නැවත පණ ගැන්වීමට (Restart):**
    ```bash
    pm2 restart all
    ```
*   **සේවාවන් ලැයිස්තුවෙන් ඉවත් කිරීමට:**
    ```bash
    pm2 delete all
    ```

### 💾 සර්වර් එක Reboot වූ විට (Persistence)
*   **දැනට රන් වන ලිස්ට් එක සේව් කිරීමට:**
    ```bash
    pm2 save
    ```
*   **සර්වර් එක Restart වූ විගස PM2 ආරම්භ වීමට:**
    ```bash
    pm2 startup
    ```
    *(මෙය ගැසූ පසු ලැබෙන පේළිය කොපි කර රන් කරන්න)*

---

## 🧹 2. System Maintenance & Disk Cleanup (නඩත්තුව)

ඩිස්ක් එක පිරීම වැළැක්වීමට සහ හිරවීම් ඉවත් කිරීමට මෙම විධානයන් භාවිතා කරන්න.

### 📂 අවසර සහ ඉඩ (Permissions & Disk)
*   **ෆෝල්ඩරයට පූර්ණ අවසර ලබා දීම:**
    ```bash
    chmod -R 777 ~/WaNTg
    ```
*   **ඉතිරිව ඇති ඉඩ පරීක්ෂා කිරීම:**
    ```bash
    df -h
    ```

### 🧽 ඉඩ නිදහස් කිරීම (Cleanup)
*   **බාගත වූ මීඩියා මකා දැමීම:**
    ```bash
    rm -rf ~/WaNTg/downloads/*
    ```
*   **ලොග් ෆයිල් හිස් කිරීම (Reset Logs):**
    ```bash
    pm2 flush
    truncate -s 0 ~/WaNTg/*.log
    ```
*   **Ubuntu අනවශ්‍ය ෆයිල් පිරිසිදු කිරීම:**
    ```bash
    sudo apt clean && sudo apt autoremove -y
    ```

### 🛑 හිරවුණු දේවල් නැවැත්වීම (Force Kill)
*   **බ්‍රවුසරය සහ PHP හිරවී ඇත්නම්:**
    ```bash
    pkill -9 -f chrome
    pkill -9 -f chromium
    pkill -9 -f php
    rm -f ~/WaNTg/*.lock
    ```

### 📏 ඩිස්ක් එක වැඩි කිරීම (Resize Partition)
සර්වර් එකේ ඉඩ වැඩි කළ පසු (8GB -> 20GB) එය පද්ධතියට එක් කිරීමට:
```bash
sudo growpart /dev/sda 1
sudo resize2fs /dev/sda1
```
---
### ⏰ 3. Cron Job Control (ස්වයංක්‍රීයකරණය)
*   **Cron Jobs සංස්කරණය කිරීමට:**
```Bash
crontab -e
```

*   **Cron සේවාව Restart කිරීමට:**
```Bash
sudo systemctl restart cron
```

---
### ⏰ 4. සර්වර් එකට "Swap Space" එකතු කිරීම
*   ඔබේ VPS එකේ RAM එක පිරුණු සැණින් පද්ධතිය Crash වීම වැළැක්වීමට අපි ඩිස්ක් එකෙන් 2GB ප්‍රමාණයක් "අතථ්‍ය මතකය" (Virtual Memory) ලෙස වෙන් කරමු. මෙය පද්ධතියේ ස්ථායීතාවය (Stability) 100% කින් වැඩි කරයි.

```Bash
sudo fallocate -l 2G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
# සර්වර් එක Restart වුණත් Swap එක වැඩ කරන්න:
echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab
```

### ⏰ 5. .conf files rename කර .dlx extension එකට වෙනස් කරන්න ඕනේ නම්
*   ඔබේ VPS එකේ RAM එක පිරුණු සැණින් පද්ධතිය Crash වීම වැළැක්වීමට අපි ඩිස්ක් එකෙන් 2GB ප්‍රමාණයක් "අතථ්‍ය මතකය" (Virtual Memory) ලෙස වෙන් කරමු. මෙය පද්ධතියේ ස්ථායීතාවය (Stability) 100% කින් වැඩි කරයි.

```Bash
for f in *.conf; do
    cp "$f" "${f%.conf}.dlx"
done
```

*   Move (rename) කරන්න ඕනේ නම් copy නොවෙයි.

```Bash
for f in *.conf; do
    mv "$f" "${f%.conf}.dlx"
done
```

```Bash
for f in *.dlx; do
    mv "$f" "${f%.dlx}.conf"
done
```

### 💡 The Emergency Combo (හදිසි අවස්ථාවකදී)
පද්ධතිය සම්පූර්ණයෙන් පිරිසිදු කර නැවත පණ ගැන්වීමට මෙය එකවර රන් කරන්න:
```Bash
pm2 flush && rm -f ~/WaNTg/*.lock && pm2 restart all && pm2 status
```

### 👨‍💻 Author
Developed by **[Erandiya Sumanaweera.](https://fb.com/erandiya)**

---