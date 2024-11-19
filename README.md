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




**Creating Multiple Domain Users via PowerShell**

In this step, we will create multiple user accounts within Active Directory using PowerShell on our domain controller (DC-1). This process involves logging into DC-1 as an administrator, utilizing PowerShell ISE to run a script that generates 1,000 users with random names.

### **Steps:**

1. **Log into DC-1 as an Administrator:**
   
   - **Connect via RDP:**
     - Open **Remote Desktop Protocol (RDP)** on your local machine.
     - Enter the **public IP address** of DC-1 and click **Connect**.
     - Log in using your domain administrator credentials (e.g., `mydomain.com\jane_admin` and your password).

2. **Open PowerShell ISE as Administrator:**
   
   - **Access PowerShell ISE:**
     - Click the **Start** button located at the bottom left corner of the screen.
     - In the search bar, type **"PowerShell ISE"**.
     - Right-click on **Windows PowerShell ISE** from the search results and select **"Run as administrator"** to open it with administrative privileges.

3. **Create and Save the PowerShell Script:**
   
   - **Create a New Script:**
     - In PowerShell ISE, click on the **New Script** button (represented by a white square) in the top left corner to open a new script file.
   
   - **Paste the Script:**
     - https://github.com/joshmadakor1/AD_PS/blob/master/Generate-Names-Create-Users.ps1
     - Copy the provided PowerShell script that generates 1,000 users with random names.
     - Paste the script into the script editor pane. *(Ensure that the script is correctly formatted and free of errors.)*
   
   - **Save the Script:**
     - Press **Ctrl + S** to save the script.
     - In the **Save As** dialog, navigate to your desired location.
     - Enter **"create_users.ps1"** as the file name and click **Save**.

4. **Run the PowerShell Script:**
   
   - **Execute the Script:**
     - With the script open in PowerShell ISE, click the **Run Script** button (typically a green arrow) located at the top of the window.
   
   - **Monitor Execution:**
     - The script will begin creating 1,000 user accounts within Active Directory.
     - Monitor the output pane for any errors or confirmation messages indicating successful user creation.

<p>
<img width="1800" alt="Screenshot 2024-11-18 at 6 58 09 PM" src="https://github.com/user-attachments/assets/2017d197-36a0-4066-8f19-fbdf0d212b6b">
</p>


<p>
<img width="883" alt="Screenshot 2024-11-18 at 9 08 12 PM" src="https://github.com/user-attachments/assets/fd959a08-3856-403f-8b89-a864aed55688">
</p>

<p>
<img width="1800" alt="Screenshot 2024-11-18 at 9 18 10 PM" src="https://github.com/user-attachments/assets/fecb8ae3-050e-48ad-be2d-7885fcd28028">
</p>
Certainly! Below is a professional, step-by-step guide for logging into Client 1 using one of the newly created user accounts.

---

### **Procedure to Log into Client 1 with a New User Account**

1. **Verify User Setup**
   - Ensure that the new user accounts have been successfully created by reviewing the setup script.
   - Confirm that all new users have the default password set to **"Password1"**.

2. **Access the Domain Controller**
   - Navigate to the **Domain Controller** within your network environment.

3. **Open Active Directory Users and Computers**
   - Locate the **Start** menu on the bottom left of the screen.
   - In the search bar, type **"Active Directory Users and Computers"** and press **Enter** to launch the application.

4. **Navigate to the Employees Organizational Unit (OU)**
   - Within the **Active Directory Users and Computers** window, select your domain, e.g., **"mydomain.com"**.
   - Expand the domain tree and navigate to the **_EMPLOYEES** organizational unit (OU) to view all newly created employee accounts.

5. **Select a User Account**
   - Browse through the list of new employee accounts generated by the script.
   - Choose a user account at random for the login test.

6. **Log into Client 1**
   - Go to **Client 1** machine.
   - On the login screen, enter the selected **username** and the default password **"Password1"**.
   - Proceed to log in to verify that the account functions correctly on Client 1.

7. **Post-Login Verification**
   - Once logged in, ensure that the user has the appropriate access and permissions as per their role.
   - Confirm that all necessary applications and resources are accessible.

<img width="1800" alt="Screenshot 2024-11-18 at 10 05 28 PM" src="https://github.com/user-attachments/assets/f726bb77-0fc8-459c-bb74-95f2645996ee">

<img width="755" alt="Screenshot 2024-11-18 at 10 06 07 PM" src="https://github.com/user-attachments/assets/00950957-3ef1-443b-aa34-2e2e3f41d4e0">

<img width="441" alt="Screenshot 2024-11-18 at 10 10 55 PM" src="https://github.com/user-attachments/assets/755f91d6-7c30-4d64-af67-03e4244a070c">

<h2>Lessons Learned</h2>

In this lab, we deployed Microsoft Azure Virtual Machines running Windows Server 2022 and Windows 10 Pro, and configured Active Directory Domain Services to centrally manage user accounts. We enabled Remote Desktop Protocol (RDP) access on Client-1 for non-administrative domain users and automated the creation of 1,000 domain user accounts using a PowerShell script. Finally, we validated the setup by logging into Client-1 with the newly created user accounts to ensure proper access and permissions.
