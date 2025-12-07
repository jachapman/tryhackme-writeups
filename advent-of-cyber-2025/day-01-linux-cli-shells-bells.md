# 🖥️ THM Advent of Cyber – Day 1: Linux CLI – Shells Bells

**Platform:** TryHackMe  
**Focus:** Linux CLI, File System Navigation, Logs, Shell Scripts

---

## 🎯 Objective

Explore the Linux command line to solve challenges and uncover hidden clues in a holiday-themed scenario.

---

## 📝 Notes / Steps

1. **Terminal Basics:**

   - `echo`, `ls`, `cat README.txt` to explore directories and files.

2. **Hidden Files:**

   - Learned that Linux hides files with a dot prefix (`.`).
   - Used `ls -la` to reveal hidden files.
   - `cat .hidden_file` revealed clues about server exploits.

3. **Log Analysis:**

   - `cd /var/log` → important security logs.
   - `grep "Failed password" auth.log` → identified suspicious SSH login attempts.

4. **Finding Scripts:**

   - `find /home/socmas -name "*egg*"` → found `eggstrike.sh`.
   - Examined script with `cat`:
     - Lines starting with `#` are comments
     - Commands: `cat wishlist.txt | sort | uniq > /tmp/dump.txt`
     - `rm wishlist.txt`, `mv eastmas.txt wishlist.txt` → attacker replaced the wishlist

5. **Server Exploration:**

   - Accessed via VM browser: `http://<IP>:8080`
   - Root-only files: `/etc/shadow` for hashed passwords (`sudo su` to elevate)

6. **Bash History:**

   - Command history stored in `.bash_history` per user.

7. **Sidequest:**
   - Explored intermediate-level hidden clues.

---

## 🔍 Key Concepts Learned

- Hidden files in Linux (`.` prefix)
- Using `ls -la`, `grep`, `find` effectively
- Shell script automation can be abused for attacks
- Logs are critical for SOC analysis

---

## 💡 Lessons / Takeaways

- Always check hidden files and logs for anomalies
- Script analysis reveals attacker intentions
- Root permissions provide critical access; practice safe elevation
- I had fun with this one and enjoyed looking for clues, as well as going through a nice Linux Command Line refresher. 

---

## 📸 Evidence
I have no screenshots to add to this one. 


