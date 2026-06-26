Splunk Logs (ACEP SOC Lab)

Welcome to the training package dataset directory. All manuals, answer keys, and project directory structures have been removed and flattened to leave only the necessary Splunk data files.

---

## 👤 ABOUT THE AUTHOR

This training program and its datasets were created by:

### **Anisetti Chaitanya Eshwar Prasad**
*Founder of AcepTech*

| Platform | Profile Link |
| :--- | :--- |
| **🌐 Website** | [chaitanyaeshwarprasad.com](https://chaitanyaeshwarprasad.com) |
| **💻 GitHub** | [github.com/chaitanyaeshwarprasad](https://github.com/chaitanyaeshwarprasad) |
| **🎥 YouTube** | [youtube.com/@chaitanya.eshwar.prasad](https://www.youtube.com/@chaitanya.eshwar.prasad) |
| **💼 LinkedIn** | [linkedin.com/in/chaitanya-eshwar-prasad](https://linkedin.com/in/chaitanya-eshwar-prasad) |
| **📸 Instagram** | [instagram.com/acep.tech.in.telugu](https://instagram.com/acep.tech.in.telugu) |
| **🐛 YesWeHack** | [yeswehack.com/hunters/chaitanya-eshwar-prasad](https://yeswehack.com/hunters/chaitanya-eshwar-prasad) |

---

## 📋 SPLUNK DATASET UPLOAD REFERENCE

Below is a reference guide for uploading the 14 flattened files in this directory to Splunk:

### 1. Standard Event Logs (Index: `main`)

For each of the following files, navigate to **Settings ➔ Add Data ➔ Upload** in Splunk. Set the **Index** to `main` and choose the corresponding **Source Type**:

| # | File Name | Recommended Source Type |
|---|---|---|
| 1 | `windows_security_logs.csv` | `csv` |
| 2 | `sysmon_events.csv` | `csv` |
| 3 | `auth.log` | `syslog` |
| 4 | `syslog.log` | `syslog` |
| 5 | `cron.log` | `syslog` |
| 6 | `firewall_logs.csv` | `csv` |
| 7 | `vpn_logs.csv` | `csv` |
| 8 | `proxy_logs.csv` | `csv` |
| 9 | `dns_logs.csv` | `csv` |
| 10 | `email_logs.csv` | `csv` |
| 11 | `powershell_logs.csv` | `csv` |
| 12 | `file_access_logs.csv` | `csv` |
| 13 | `usb_activity_logs.csv` | `csv` |

---

### 2. Lookup Tables (File-based Lookup)

The following file is a lookup table to map and enrich usernames with employee details (real name, job title, department, etc.):

*   **File Name:** `user_accounts.csv`
*   **Splunk Configuration:**
    1. Go to **Settings ➔ Lookups ➔ Lookup table files ➔ New Lookup Table File**.
    2. Set **Destination App** to `search`, choose `user_accounts.csv`, and name the destination filename `user_accounts.csv`.
    3. Go to **Settings ➔ Lookups ➔ Lookup definitions ➔ New Lookup Definition**.
    4. Set name and lookup file to `user_accounts.csv`, type to `File-based`, and save.
