# Volunteer Management App 🚀  
A **Salesforce App** to manage **volunteers and events**, allowing organizations to assign volunteers to different events while tracking their skills and availability.  

## 🔥 Features  
✅ **Volunteer Records** – Store volunteer information (Name, Email, Skills, Availability).  
✅ **Event Management** – Create and manage events with location, date, and volunteer requirements.  
✅ **Volunteer Assignments** – Track which volunteers are assigned to which events.  
✅ **Automation** – When a volunteer is assigned to an event, their **Status updates to "Active"** automatically.  

## 🛠️ Objects & Fields  
### **1️⃣ Volunteer**  
- **Volunteer Name** (Text)  
- **Email** (Email)  
- **Phone** (Phone)  
- **Availability** (Picklist: Weekdays, Weekends, Anytime)  
- **Skills** (Multi-Select Picklist)  
- **Status** (Picklist: Active, Inactive, Pending)  
- **Notes** (Long Text Area)  

### **2️⃣ Event**  
- **Event Name** (Text)  
- **Date** (Date)  
- **Location** (Text)  
- **Description** (Long Text Area)  
- **Volunteers Needed** (Number)  

### **3️⃣ Volunteer Assignment** (Junction Object)  
- **Volunteer** (Lookup → Volunteer)  
- **Event** (Lookup → Event)  
- **Role** (Picklist: Organizer, Assistant, Participant)  
- **Status** (Picklist: Assigned, Confirmed, Cancelled)  
- **Hours Worked** (Number)  

## ⚡️ Automation with Flow  
- A **Record-Triggered Flow** updates the **Volunteer’s Status to "Active"** when they are assigned to an event.  
- **Trigger:**
  - Initially: `"Only when a record is created"` ❌ (Issue: Didn’t update existing volunteers)
  - Fixed: **"When a record is created or updated"** ✅ (Now updates all Volunteers)

## 🎯 How It Works  
1️⃣ **Admin/Sales Rep Creates a New Event.**  
2️⃣ **A Volunteer is Assigned to the Event.**  
3️⃣ **Flow Runs → Automatically Updates the Volunteer’s Status to "Active".**  
4️⃣ **Volunteer’s Status is tracked in the system.**  

## 🏗️ Future Enhancements  
🔹 Add **Reports & Dashboards** for tracking Volunteer contributions.  
🔹 Automate **Volunteer Reminders** via Email.  
🔹 Create a **Volunteer Experience Log** to track past events.  

## 🌐 Deployment  
✅ Fully deployed and tested in **Salesforce Developer Org**.  
✅ Managed via **App Manager** with custom **Tabs & Page Layouts**.  
✅ Ready for **real-world use**.  

---

### **📢 Next Steps**
✅ **I’ll now modify your HTML file to include this README information** in your GitHub portfolio.  
📩 **Send me your HTML file, and I’ll update it for you!** 🚀🔥  
