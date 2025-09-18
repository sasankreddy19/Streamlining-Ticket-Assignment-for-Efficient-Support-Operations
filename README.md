# Streamlining-Ticket-Assignment-for-Efficient-Support-Operations

## 📌 Overview  
This project demonstrates how to manage **Groups, Roles, Tables, Access Control, and Flow Automation** in ServiceNow.  
It provides a hands-on exercise to understand:  
- User and role management  
- ACLs (Access Control Lists)  
- Flow Designer for ticket automation  

---

## 🛠️ Project Steps  

### 1. Create Groups  
1. Open ServiceNow.  
2. Navigate to **All → Groups** under *System Security*.  
3. Create groups such as:  
   - **Certificates Group**  
   - **Platform Group**  
4. Assign a manager and description for each group.  
5. Click **Submit**.  

---

### 2. Assign Roles & Users to Groups  

#### Certificates Group  
- Add **Katherine Pierce** as a member.  
- Assign the role **Certification_role**.  

#### Platform Group  
- Add **Manne Niranjan** as a member.  
- Assign the role **Platform_role**.  

---

### 3. Assign Role to a Table  
1. Open ServiceNow.  
2. Navigate to **All → Tables** under *System Definition*.  
3. Select the **Operations Related** table.  
4. Go to **Application Access**.  
5. Add the following roles:  
   - **Platform_role**  
   - **Certification_role**  
6. Update **Access Control** to restrict table usage based on these roles.  

---

### 4. Create Access Control (ACL)  
- Define **Access Control Rules** for the table.  
- Ensure only users with the required roles can perform **read/update** operations.  

---

### 5. Create Flows in Flow Designer  

#### Flow 1: Assign Operations Ticket to Certificate Group  
1. Open **Flow Designer** under *Process Automation*.  
2. Create a new flow → Name: **Regarding Certificate**.  
3. Set Application: **Global**.  
4. Trigger: On **Create or Update Record** in *Operations Related* table.  
5. Condition:  
   - If *Issue = Regarding Certificate*  
6. Action: Assign ticket to **Certificate Group**.  

#### Flow 2: Assign Operations Ticket to Platform Group  
1. Create a new flow → Name: **Regarding Platform**.  
2. Set Application: **Global**.  
3. Trigger: On **Create or Update Record** in *Operations Related* table.  
4. Conditions:  
   - If *Issue = Unable to login to platform*  
   - If *Issue = 404 Error*  
5. Action: Assign ticket to **Platform Group**.  

---

## 🚀 Key Learnings  
- How to create and manage **Groups** and **Roles** in ServiceNow.  
- How to assign **Users and Roles** to Groups for structured access.  
- How to configure **Access Control Lists (ACLs)** for secure table operations.  
- How to automate **ticket assignment** using Flow Designer.  

---

## 📂 Project Outcome  
By the end of this project:  
- Groups (**Certificates**, **Platform**) are created and managed.  
- Roles are assigned to enforce **role-based access control**.  
- ACLs ensure secure table access.  
- Flow automation intelligently assigns tickets to the right groups.  

---

👉 This project is a **mini end-to-end ServiceNow implementation** for **access control and automated ticket assignment**.  
