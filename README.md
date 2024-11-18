<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>
# Creating-users-with-powershell
Using PowerShell to streamline and automate domain administration.

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 Pro (21H2)

<h2>Deployment Steps</h2>
<p>
In this lab, we configured Client-1 to allow non-admin domain users to log in via Remote Desktop Protocol (RDP) and created multiple domain user accounts using PowerShell.
</p>

 **Configuring RDP Access for Domain Users and Creating Users via PowerShell**

**Configuring Remote Desktop Access for Domain Users on Client-1**

In this step, we will configure Client-1 to allow non-admin domain users to access it via Remote Desktop Protocol (RDP). This setup ensures that regular domain users can remotely access Client-1 without requiring administrative privileges.

### **Steps:**

1. **Log into Client-1 as a Domain Administrator:**
   
   - **Initiate RDP Connection:**
     - Open **Remote Desktop Protocol (RDP)** on your local machine.
     - Enter Client-1's **public IP address** and click **Connect**.
   
   - **Authenticate:**
     - On the login screen, enter the domain administrator credentials:
       - **Username:** `mydomain.com\jane_admin`
       - **Password:** [Enter the password for `jane_admin`]
     - Click **OK** to log in.

2. **Access System Properties:**
   
   - **Open System Settings:**
     - Right-click the **Start** button located at the bottom left corner of the screen.
     - Select **System** from the context menu to open the System settings window.

3. **Configure Remote Desktop Settings:**
   
   - **Open Remote Desktop Settings:**
     - In the **System** window, find and click on **Remote Desktop** in the left-hand menu.
   
   - **Enable Remote Desktop:**
     - Toggle the **Enable Remote Desktop** switch to **On**.
     - Confirm any prompts that appear to enable Remote Desktop.

4. **Allow Remote Users to Access Client-1:**
   
   - **Select Users for Remote Access:**
     - In the **Remote Desktop** settings, scroll down and click on **Select users that can remotely access this PC**.
   
   - **Add Domain Users Group:**
     - In the **Remote Desktop Users** window, click on the **Add** button.
     - In the **Select Users or Groups** dialog box, type **Domain Users**.
     - Click **Check Names** to validate the group name.
     - Once the name is recognized, click **OK** to add the group.
   
   - **Apply Changes:**
     - Click **OK** to confirm and close the **Remote Desktop Users** window.

5. **Finalize Configuration:**
   
   - **Confirm Settings:**
     - Ensure that the **Domain Users** group is listed in the **Remote Desktop Users** window.
     - This confirms that all domain users will have RDP access to Client-1 without requiring administrative privileges.
   
   - **Close System Settings:**
     - Close the **System** window to complete the configuration.


<p>
 <img width="437" alt="Screenshot 2024-11-18 at 5 17 51 PM" src="https://github.com/user-attachments/assets/a174439f-badd-4634-b1ea-68c59b4a0552">
</p>  

<p> 
<img width="1800" alt="Screenshot 2024-11-18 at 5 25 57 PM" src="https://github.com/user-attachments/assets/8a62898b-c33b-4222-8b93-e0aedc736b7e">
</p>

<p>
<img width="1197" alt="Screenshot 2024-11-18 at 6 38 51 PM" src="https://github.com/user-attachments/assets/2ff07467-4f59-4de6-8300-57ffa151a637">
</p>

<p>
<img width="1198" alt="Screenshot 2024-11-18 at 5 31 00 PM" src="https://github.com/user-attachments/assets/56065988-0abf-4c02-b941-c6cc9b4602c2">
</p>

<p>
<img width="454" alt="Screenshot 2024-11-18 at 5 47 56 PM" src="https://github.com/user-attachments/assets/ad6c3a0a-f39d-4dd9-8ef5-359edf10684d">
</p>


