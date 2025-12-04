# 🏥 Medical Test Prerequisite Automation (n8n + Gemini + SMTP)

An automated workflow built using **n8n**, **Google Gemini**, and **SMTP email** to instantly send patient-friendly medical test instructions based on the test selected in an online form.

This system reduces manual work for diagnostic centers and ensures patients always receive clear, accurate prerequisites.

---

## 🚀 Features

- 📋 **Dynamic form input** using n8n Form Trigger  
- 🔀 **Conditional routing** for different test types (Blood Test, MRI, Ultrasound, CT Scan)  
- 🤖 **Gemini LLM rewriting** for clear, patient-friendly instructions  
- 📧 **Automated email delivery** using SMTP (Gmail App Password)  
- ⚙️ **End-to-end workflow:** Form → Switch → LLM → Email  

---

## 🧠 Tech Stack

| Category | Tools |
|---------|-------|
| Automation | n8n |
| AI | Google Gemini (Text Generation) |
| Email Service | SMTP (Gmail App Password) |
| Logic | Switch Nodes, Set Nodes |
| Format | Workflow JSON Export |

---

## 🛠 Workflow Architecture

### 1. **Form Trigger (Patient Input)**
Patients submit:
- Full Name  
- Email  
- Phone Number  
- Selected Test/Scan  

### 2. **Switch Node (Routing by Test)**
Routes input to the correct prerequisite based on:
- Blood Test  
- MRI  
- Ultrasound  
- CT Scan  

### 3. **Set Nodes (Static Prerequisites)**
Each test has precise predefined instructions.

### 4. **LLM Node — Google Gemini**
Rewrites prerequisites into:
- patient-friendly,  
- simple,  
- medically accurate text.

### 5. **Email Node**
Sends the final instructions to the patient using SMTP.

---

## 📁 Files Included

```
Medical Test Prerequisite Automation.json
README.md
```

---

## 📥 Importing the Workflow into n8n

1. Open your n8n instance.  
2. Click **Workflows → Import from File**.  
3. Select the JSON file:  
   ```
   Medical Test Prerequisite Automation.json
   ```  
4. Add your own:
   - Gemini API key  
   - SMTP credentials  
5. Activate the workflow.  

---

## 📧 SMTP Setup (Gmail)

To use Gmail for sending emails:

1. Enable **2-Step Verification**  
2. Create an **App Password**  
3. Create a new **SMTP credential** in n8n:  

```
Host: smtp.gmail.com
Port: 465
User: your-email@gmail.com
Password: <APP_PASSWORD>
SSL/TLS: ON
```

---

## 🧪 Testing the Workflow

1. Activate the workflow.  
2. Open the **Production URL** from the Form Trigger.  
3. Fill the form as a patient would.  
4. Check your email for the instructions.  

---

## 📝 Example Output Email

```
Hello John Doe,

Here are the instructions for your upcoming test: MRI

Please remove all metal objects before your MRI scan, including jewelry, watches, belts, and hair accessories...

Thank you,
Your Medical Centre
```

---

---

## 📄 License

This project is open-source and available under the **MIT License**.

