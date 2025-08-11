
This is an automated content idea tool built on n8n. It captures new content ideas from a Google Sheet, sends them to the right team members by email, and logs each idea as a task in ClickUp.

## What It Does

This workflow watches a Google Sheet for new content ideas, routes each idea based on category to the appropriate team, sends personalized emails with the idea details, and creates tasks in ClickUp for tracking — all automatically.

---

## 📌 Features

- Google Sheets trigger for new ideas  
- Conditional routing based on idea category  
- Customized email notifications to multiple staff members  
- Task creation in ClickUp for easy management  
- Built with n8n (open-source automation tool)  

---

## ⚙️ Technologies

- n8n  
- Google Sheets Trigger Node  
- Switch Node (for routing)  
- Set Nodes (to format data and emails)  
- SMTP Email Nodes  
- ClickUp Node (task creation)  

---

## 🔧 How It Works

1. **Google Trigger** – Detects new content ideas added to the sheet.  
2. **Set Node** – Prepares idea data for processing.  
3. **Switch Node** – Routes the idea to the correct team based on category.  
4. **Set Nodes** – Create custom email content per team.  
5. **Send Email Nodes** – Sends the idea to appropriate staff members.  
6. **Merge Node** – Combines email send outputs.  
7. **ClickUp Node** – Creates a task in ClickUp to track the idea.

---

## 📬 Example Output
<img width="769" height="508" alt="Screenshot 2025-08-11 at 17 47 49" src="https://github.com/user-attachments/assets/2084b4c7-de67-40b0-b31f-bb5ca7207748" />



---

## Workflow

```mermaid
flowchart LR
    A[Google Trigger] --> B[Set Node]
    B --> C[Switch Node]
    C -->|Team A| D[Set Node - Team A Email]
    C -->|Team B| E[Set Node - Team B Email]
    C -->|Team C| F[Set Node - Team C Email]
    D --> G[Send Email - Team A]
    E --> H[Send Email - Team B]
    F --> I[Send Email - Team C]
    G & H & I --> J[Merge Node]
    J --> K[ClickUp Node]

Skills Learned
Connecting and authenticating Google Sheets and ClickUp APIs

Building dynamic email workflows with n8n

Using Switch nodes for conditional logic

Automating team communication and task management

💡 Why I Built This
I wanted a reliable way to capture new content ideas from the team and automatically notify the right people, while keeping everything organized in ClickUp. This project helped me learn how to build powerful no-code automations with n8n to streamline content workflows.

Follow me on LinkedIn to see more of my automation journey.
