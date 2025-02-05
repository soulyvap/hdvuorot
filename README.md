Here's your **finalized Technical Write-up** with the **requested images** integrated for a professional and well-structured document. 🚀  

---

# **HDVUOROT – A Shared Calendar for IT Helpdesk Teams**  

## **Project Overview**
**HDVUOROT** is an internal platform designed to help IT helpdesk workers keep track of each other's **availability statuses**. The application provides a **shared calendar interface** where users can log future **absences, remote working days, and other schedule-related updates**.  

This system is particularly valuable for IT teams that rely on **coordinated availability** to handle support requests efficiently. The platform was developed to replace **manual tracking methods** and improve **visibility and scheduling** within the team.  

Due to company restrictions, the source code is private, but this document serves as a **technical write-up** to outline the development process, architecture, and key challenges.

---

## **Project Screenshots**  

### **Home Page - Table View**  
📌 **Visualize coworkers' statuses for a month**  
📌 **Sort and filter by name, title, unit, location, and status**  

<img width="1680" alt="Home Page - Table View" src="https://github.com/user-attachments/assets/2a58b45e-c556-42b9-9362-9d1674f3fa2f" />

---

### **Home Page - Edit Mode**  
📌 **Edit your own availability statuses**  
📌 **Admins can modify other users' statuses**  

<img width="1680" alt="Home Page - Edit Mode" src="https://github.com/user-attachments/assets/c9fae500-67b8-462e-b53d-43109923d4a9" />

---

### **Home Page - Calendar View**  
📌 **Visualize coworkers' statuses for a week**  
📌 **Sort by status**  

<img width="1680" alt="Home Page - Calendar View" src="https://github.com/user-attachments/assets/fa677e79-09e0-45c4-9f5d-f5f2eaa0cc9e" />

---

### **Admin Page - User Management View**  
📌 **Admins can add, delete, and edit users**  

<img width="1680" alt="Admin Page - User Management View" src="https://github.com/user-attachments/assets/23d0c84c-cf70-46a0-bac2-3c4afd52fb90" />

---

### **Admin Page - Unit Management View**  
📌 **Admins can add, delete, and edit employee units**  

<img width="1680" alt="Admin Page - Unit Management View" src="https://github.com/user-attachments/assets/d731f52e-43bb-44e9-81e2-6947a92625da" />

---

### **Admin Page - Logs View**  
📌 **Admins can visualize change logs**  

<img width="1680" alt="Admin Page - Logs View" src="https://github.com/user-attachments/assets/05119395-5039-4b93-945c-41410df80a26" />

---

### **Home Page - Table View (Mobile)**  
📌 **Mobile-friendly view for quick status checking**  

<img width="369" alt="Home Page - Mobile View" src="https://github.com/user-attachments/assets/ccec5245-a50f-416e-b16e-5d2be4aa1bef" />

---

## **Technology Stack**
HDVUOROT is built using **modern web technologies**, emphasizing **scalability, security, and maintainability**.  

### **Frontend**
- **Framework**: Next.js 14 (React-based, supports SSR & SSG for performance optimization)
- **State Management**: Zustand (lightweight alternative to Redux)
- **Authentication**: OAuth via Azure AD
- **Styling**: TailwindCSS  

### **Backend**
- **Framework**: Node.js with Express.js
- **Database**: SQLite, managed using Sequelize ORM
- **Authentication**: JWT-based authentication

### **DevOps & Deployment**
- **CI/CD**: Automated pipelines using GitLab CI/CD
- **Containerization**: Docker
- **Infrastructure**: Hosted on a cloud provider (details omitted for security)
- **Security**: Role-based access control (RBAC), environment variable encryption

---

## **System Architecture**
HDVUOROT follows a **three-tier architecture**, ensuring separation of concerns and scalability.  

### **Authentication Flow**
1. Users sign in via **Azure AD OAuth**.
2. Backend verifies the **OAuth token** and issues a **JWT**.
3. The JWT is used to authenticate API requests.

### **CI/CD Pipeline**
- **Automated builds & testing** using **GitLab CI/CD**.
- **Dockerized deployments** for portability.
- **Automated database migrations** using Sequelize.

---

## **Development Process & Challenges**
### **1️⃣ Authentication & Security**
**Challenge**: Implementing **secure enterprise authentication** while keeping user sessions lightweight.  
**Solution**: Used **OAuth with Azure AD**, replacing **traditional email/password logins**. Sessions are managed with **JWT tokens**, reducing server load.

### **2️⃣ CI/CD & Deployment**
**Challenge**: Automating deployments while ensuring **zero downtime**.  
**Solution**: Implemented **GitLab CI/CD** with **Dockerized containers** for easy rollbacks.

---

## **Future Improvements**
🔹 **Integration with external scheduling tools** (e.g., Google Calendar API)  
🔹 **Event-based architecture** (using Kafka or Pub/Sub) for real-time updates  

---

## **Conclusion**
HDVUOROT is a **fully functional shared calendar system**, improving **team coordination and efficiency**. This project solidified my skills in **TypeScript, cloud infrastructure, security best practices, and CI/CD automation**—all of which are highly relevant for Veikkaus.  

Although the repository is private, I’d be happy to discuss the **architecture and implementation** in more detail. Feel free to reach out!
