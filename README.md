# 🏛️ Lab: Install and Configure Active Directory Certificate Services (AD CS) on Windows Server 2019

## 📚 Lab Overview
This lab demonstrates how to install and configure **Active Directory Certificate Services (AD CS)** in a Windows Server 2019 environment. You'll set up a Root Certificate Authority (CA), configure Web Enrollment, and verify the functionality of your internal PKI infrastructure.

---

## 🛠️ Key Skills Practiced
- Windows Server Role & Feature Management  
- Active Directory Certificate Services (AD CS) setup  
- Configuring a Root Certificate Authority  
- Enabling Web Enrollment with IIS  
- Public Key Infrastructure (PKI) fundamentals  
- Verifying CA operation and certificate issuance  
- Integration of AD CS with Active Directory Domain

---

## 🖥️ Lab Environment
- **Operating System**: Windows Server 2019 Standard Evaluation  
- **Processor**: Intel(R) Core(TM) i9-9880H CPU @ 2.30GHz  
- **Memory**: 4 GB RAM  
- **System Type**: 64-bit OS, x64-based processor  
- **Domain**: `mylab.local`  
- **Computer Name**: WIN-FJ30ND3AI67  

📸 `screenshots/01_system_info.png`

---

## 🪜 Step-by-Step Instructions

### 🔹 1. Launch Add Roles and Features Wizard  
Open Server Manager and start the **Add Roles and Features** wizard. Choose **Role-based or feature-based installation**.

📸 `screenshots/02_add_roles_adcs.png`

---

### 🔹 2. Select AD CS Role  
Select **Active Directory Certificate Services**. When prompted, add required features.

📸 `screenshots/02_add_roles_adcs.png`

---

### 🔹 3. Add IIS Web Enrollment Features  
To enable Web Enrollment, IIS features must be installed (ASP.NET, ISAPI Extensions, etc.).

📸 `screenshots/03_add_features_iis.png`

---

### 🔹 4. Confirm Selections and Install  
Verify that the roles and features listed are correct and allow the system to reboot if needed.

📸 `screenshots/04_confirm_installation.png`

---

### 🔹 5. Configure AD CS Role Services  
Select the role services:
- ✅ Certification Authority  
- ✅ Certification Authority Web Enrollment

📸 `screenshots/05_configure_role_services.png`

---

### 🔹 6. Choose CA Type  
Select **Root CA** — this creates a self-signed certificate and establishes a trusted root.

📸 `screenshots/06_ca_type_root.png`

---

### 🔹 7. Set Certificate Validity Period  
Leave the default of **5 years** or adjust as needed.

📸 `screenshots/07_validity_period.png`

---

### 🔹 8. Open the Certification Authority Console  
Go to **Tools > Certification Authority** in Server Manager to manage your CA.

📸 `screenshots/08_open_cert_authority.png`

---

### 🔹 9. Verify CA Is Active  
Ensure your Root CA appears and is running. Browse through folders like:
- Issued Certificates  
- Revoked Certificates  
- Pending Requests  
- Certificate Templates

📸 `screenshots/09_cert_authority_loaded.png`  
📸 `screenshots/10_cert_authority_options.png`

---

## 📁 Project Structure

