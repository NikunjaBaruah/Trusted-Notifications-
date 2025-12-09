# Trusted Notifications Prototype – Bank

This is a simple web-based prototype to demonstrate a **Trusted Notification Framework** for a bank.  
It is built using only **HTML, CSS, and JavaScript (no backend / no database)**.

The goal is to show how a bank can:
- Configure different notification events (e.g., Login OTP, High Value Debit)
- Decide which **channels** to use (SMS, Email, App Push, In-App)
- Apply **fallback logic** if the primary channel fails
- Provide a **Trusted Notification Center** where customers can verify genuine alerts

---

## Features

### 1. Admin – Configure Events
- Add or update notification events with:
  - Event name  
  - Priority (High / Medium / Low)  
  - Risk level (High / Low)  
  - Primary channel  
  - Secondary (fallback) channel  
  - Retry time in seconds  
- Events are stored in a simple JavaScript array (`events`).

### 2. Simulate Events
- Select an event and user, enter amount (for debit events), and simulate:
  - Generates a notification message (OTP / debit / offer / generic)
  - Applies **primary channel** and, if “SMS failure” is selected, uses **fallback channel**
  - Logs what happened (delivered via primary or fallback / failed)

### 3. Customer – Trusted Notification Center
- Shows all generated notifications in a scrollable list.
- Clicking a notification shows details:
  - Title, time, channel used, status
  - **Trust markers**: masked account number, security phrase, customer name
  - Event details: priority, risk level, channels, retry time
- “Mark all as read” button to update notification status.

---

## How to Run

   - 1. Admin – Configure Events** → define or edit events  
   - 2. Simulate Events** → trigger sample notifications  
   - 3. Customer Notifications** → view trusted notifications


