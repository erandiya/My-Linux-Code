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

ඔබේ VPS එකේ කටයුතු පහසු කර ගැනීම සඳහා PM2 (Process Manager 2) හි භාවිතා වන වැදගත්ම කමාන්ඩ් (Commands) ටික මෙන්න. මෙය ඔබට ඕනෑම වෙලාවක බලා ගැනීමට "Cheat Sheet" එකක් ලෙස පාවිච්චි කළ හැක.
🚀 1. වැඩසටහන් ආරම්භ කිරීම (Starting)
pm2 start index.js --name "whatsapp-api"
අලුතින් ස්ක්‍රිප්ට් එකක් නමක් සහිතව ආරම්භ කිරීමට.
pm2 start index.js -i max
සර්වර් එකේ තියෙන සියලුම CPU Cores භාවිතා කරමින් (Cluster mode) රන් කිරීමට.
📊 2. තත්ත්වය පරීක්ෂා කිරීම (Monitoring)
pm2 status (හෝ pm2 list)
දැනට රන් වන සියලුම වැඩසටහන් වල ලැයිස්තුව සහ ඒවායේ තත්ත්වය (Online/Stopped) බැලීමට.
pm2 logs
සියලුම වැඩසටහන් වල සජීවී ලොග් (Messages/Errors) බැලීමට.
pm2 logs whatsapp-api
එක් විශේෂිත වැඩසටහනක ලොග් පමණක් බැලීමට.
pm2 monit
සර්වර් එකේ CPU සහ RAM භාවිතය ඉතා ලස්සනට (Dashboard එකක් ලෙස) බැලීමට.
🔄 3. පාලනය කිරීම (Control)
pm2 stop all
දැනට රන් වන සියලුම වැඩසටහන් නැවැත්වීමට.
pm2 restart all
සියලුම වැඩසටහන් නැවත පණ ගැන්වීමට (Restart).
pm2 reload all
Zero-downtime restart (වැඩසටහන සම්පූර්ණයෙන්ම නතර නොකර අලුත් කේතයන් ලබා ගැනීමට).
pm2 delete all
ලැයිස්තුවෙන් සියලුම වැඩසටහන් සම්පූර්ණයෙන්ම ඉවත් කිරීමට.
💾 4. සර්වර් එක Reboot වුවහොත් (Persistence)
pm2 save
දැනට රන් වන ලිස්ට් එක සේව් කිරීමට (සර්වර් එක Restart වුවහොත් මේ ලිස්ට් එකම නැවත පණ ගැන්වේ).
pm2 startup
සර්වර් එක ඔන් වන විටම PM2 ස්වයංක්‍රීයව ආරම්භ වීමට අවශ්‍ය කේතය ලබා ගැනීමට (මෙය ගැසූ පසු ලැබෙන පේළිය කොපි කර රන් කරන්න).
🧹 5. නඩත්තුව (Maintenance)
pm2 flush
පරණ Log ෆයිල්ස් ඔක්කොම මකා දමා Disk Space නිදහස් කිරීමට (ඉතා වැදගත්).
pm2 update
PM2 මෘදුකාංගය අලුත් (Update) කිරීමට.
💡 නිතරම භාවිතා වන පේළිය (The Combo):
ඔබ කේතයේ (Code) වෙනසක් කළ පසු පද්ධතිය සම්පූර්ණයෙන් පිරිසිදු කර නැවත පණ ගැන්වීමට මෙය භාවිතා කරන්න:
code
Bash
pm2 flush && pm2 restart all && pm2 status
මෙම සටහන ඔබේ පද්ධතිය පාලනය කිරීමට ගොඩක් උදව් වේවි! තව මොනවා හරි දැනගන්න ඕනෙද?

---

### 👨‍💻 Author
Developed by **[Erandiya Sumanaweera.](https://fb.com/erandiya)**

---