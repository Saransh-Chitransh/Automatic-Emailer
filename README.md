# 📧 Auto Email Sender using Python & Google Sheets

This project automates the process of sending personalized emails (along with attachments like resumes) to a list of recipients directly fetched from a Google Sheet.

It supports:
- Fetching email addresses from Google Sheets  
- Custom email body (from a `.txt` file)  
- Sending attachments (e.g., Resume in PDF)  
- Progress bar while sending using `tqdm`  
- Error handling for file and SMTP issues  

---

## 📁 Folder Structure
```
.
├── Auto_Emailer.txt             # Email body content
├── Your_Resume.pdf              # File to be attached with each email
├── send_emails.py               # Python script
└── README.md                    # This file
```

---

## ✅ Requirements

- Python 3.7+
- Packages:
  - `pandas`
  - `tqdm`

Install them with:
```bash
pip install pandas tqdm
```

---

## 🧾 Google Sheet Setup

1. Open your Google Sheet with recipient emails (email addresses in the **first column**).
2. Click `Share` > `Anyone with the link can view`.
3. Get the CSV export link:

   ```
   https://docs.google.com/spreadsheets/d/<your-sheet-id>/export?format=csv
   ```

4. Replace the `sheet_url` in the script with your link.

---

## ✉️ Gmail Setup

- Enable **2-Step Verification** in your Google Account.
- Generate an **App Password** from your [Google Account Security](https://myaccount.google.com/security) page.
- Use this app password in the script instead of your normal password.

---

## 🛠️ How to Use

1. Add your email content to `Auto_Emailer.txt`.
2. Add your resume (or any attachment) and update the `attachment_path` in the script.
3. Replace placeholders in the script:
   - Your email
   - App password
   - Subject line
   - Sheet URL
4. Run the script:
```bash
python send_emails.py
```

---

## 📤 Output

- Sends emails one by one with a live progress bar.
- Shows final completion time.
- Error messages will appear for invalid email addresses, attachment errors, or failed SMTP connections.

---

## ⚠️ Notes

- Avoid using your real password—**always use app-specific passwords**.
- You can expand this script to include personalized greetings using `pandas` if names are available in the sheet.

---

## 🤝 Contribute

Feel free to fork and improve this script. Add support for CC/BCC, HTML formatting, or Gmail API!

---
