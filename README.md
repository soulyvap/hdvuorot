# **HDVUOROT**

## **Project Overview**
**HDVUOROT** is an internal platform designed to help IT helpdesk workers keep track of each other's **availability statuses**. The application provides a **shared calendar interface** where users can log future **absences, remote working days, and other schedule-related updates**.  

This system is particularly valuable for IT teams that rely on **coordinated availability** to handle support requests efficiently. The platform was developed to replace **manual tracking methods** and improve **visibility and scheduling** within the team.  

Due to company restrictions, the source code is private, but this document serves as a **technical write-up** to outline the development process, architecture, and key challenges.

---

## **Project Screenshots**  

### **Home Page - Table View**  
📌 **Visualize coworkers' statuses for a month**  
📌 **Sort and filter by name, title, unit, location, and status**  

![Slide6](https://github.com/user-attachments/assets/b5820c9d-ef90-4020-a036-98779180e3ee)

---

### **Home Page - Edit Mode**  
📌 **Edit your own availability statuses**  
📌 **Admins can modify other users' statuses**  

![Slide5](https://github.com/user-attachments/assets/88a7a07c-e1eb-4e94-a85a-7d52fdf4e6b9)

---

### **Home Page - Calendar View**  
📌 **Visualize coworkers' statuses for a week**  
📌 **Sorted by status**  

![Slide1](https://github.com/user-attachments/assets/638b33df-e055-4bfa-bacb-d6e3ded691f8)

---

### **Admin Page - User Management View**  
📌 **Admins can add, delete, and edit users**  

![Slide4](https://github.com/user-attachments/assets/97df6ba6-f9fc-42db-a5ef-dba3550c4b94)

---

### **Admin Page - Unit Management View**  
📌 **Admins can add, delete, and edit employee units**  

![Slide3](https://github.com/user-attachments/assets/6017d49c-5fcc-4b73-9fa0-67fc70ffdea3)

---

### **Admin Page - Logs View**  
📌 **Admins can visualize change logs**  

![Slide2](https://github.com/user-attachments/assets/70b1f3e1-c284-4868-9ed3-9a91f45bbec5)

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
