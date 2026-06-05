
### 🧰 What `crontab` is good for:

|Use Case|Example|
|---|---|
|✅ Run scripts at specific times|Backup a database at midnight|
|✅ Run commands periodically|Clean temp files every hour|
|✅ Run something **at boot**|Start a custom app or script|
|✅ Automate system maintenance|Rotate logs, restart services|
|✅ Trigger webhooks/APIs|Curl a URL daily for updates|

---

### Breaking down the cron syntax:

`*/10 * * * *` means:

|Field|Value (`*` means “every”)|Meaning|
|---|---|---|
|Minute|`*/10`|Every 10 minutes|
|Hour|`*`|Every hour|
|Day of month|`*`|Every day of the month|
|Month|`*`|Every month|
|Day of week|`*`|Every day of the week|

So overall, it means:  
**Run the command every 10 minutes, regardless of hour, day, month, or weekday.**

---

If you want it to run less often, you change those other fields. For example:

- `0 3 * * *` → at 3:00 AM every day
    
- `0 18 * * 1` → at 6:00 PM every Monday

---

### 💡 Common Time Examples

|Schedule|Crontab Line|
|---|---|
|Every 5 minutes|`*/5 * * * *`|
|Every day at 3am|`0 3 * * *`|
|Every Monday at 6pm|`0 18 * * 1`|
|At system boot|`@reboot`|

---

### 🛠 Example: Run a script every 10 minutes using `cron`

Assume your script is:

```swift
/usr/local/bin/myscript.sh
```

Make sure it’s executable:

```bash
chmod +x /usr/local/bin/myscript.sh
```

---

### 1. Open the crontab editor:

```bash
crontab -e
```

---

### 2. Add this line at the bottom:

```pearl
*/10 * * * * /usr/local/bin/myscript.sh

```
- `*/10` = every 10 minutes
    
- Rest = every hour, every day, etc.
    

---

### ✅ Save and exit

That’s it! The script will now run every 10 minutes. You can verify it’s installed with:

```bash
crontab -l
```

---

### 📝 To run at boot only (with cron):

Add this instead:

```swift
@reboot /usr/local/bin/myscript.sh
```