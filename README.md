# Ancora-Education-Ucertify-Lab9
# Configuring Clientless SSL VPNs on ASA

A Clientless Secure Sockets Layer (SSL) Virtual Private Network (VPN) allows remote users to securely access internal network resources using a web browser without installing any VPN client software. This type of VPN is commonly used for providing secure remote access to corporate applications and services. Cisco Adaptive Security Appliance (ASA) provides a graphical configuration interface called the Cisco Adaptive Security Device Manager (ASDM). ASDM simplifies VPN configuration through interactive wizards, allowing administrators to configure complex security features without manually entering command-line commands.

> **Original Lab Source**
> This lab was available through:
> [https://ancoraeducation.ucertify.com/app/?func=navigate_items&item_sequence=1]

## Objective of the Lab
This lab session demonstrates the steps involved in configuring clientless SSL VPNs on ASA. Upon completion of this lab, you will be able to: 

  Launch ASDM and configure the clientless SSL VPN.
  
  Configure user authentication, create and test the group policy.

## Instructions
## PART A: Launching ASDM and Configuring the Clientless SSL VPN
### STEP 1
On the desktop, double-click the ASDM icon.

### STEP 2
In the Cisco ASDM-IDM Launcher v1.8(0) dialog box, in the Password text box, type (ucertify) and keep the remaining settings as default, and click OK.

**Caution**

At the Security Warning prompt, click Continue. 

Wait for some time for ASDM to launch. 

At the Upgrade Image prompt, click Continue Without Upgrade.

### STEP 3
In the Cisco ASDM 7.3 for ASA - asa window, from the menu bar, navigate to Wizards > VPN Wizards > Clientless SSL VPN Wizard.

### STEP 4
In the SSL VPN Wizard dialog box, at Clientless SSL VPN Connection, click Next >.

### STEP 5
Under SSL VPN Interface, in Connection Profile Name, type (NY-connection-profile) and from the SSL VPN Interface list, select management.

### STEP 6
Under Digital Certificate, click Manage.

### STEP 7
In the Manage Identity Certificates dialog box, click Add.

### STEP 8
In the Add Identity Certificate dialog box, select Add a new identity certificate and click New.

### STEP 9
In the Add Key Pair dialog box, select Enter new key pair name, and in the text box, type (first-key-pair), then click Generate Now.

### STEP 10
In the Add Identity Certificate dialog box, click Select next to Certificate Subject DN

### STEP 11
In the Certificate Subject DN dialog box, from the Attribute list, select Common Name (CN), and in the Value text box, type (192.168.1.207), click Add >>, and then click OK.

### STEP 12
In the Add Identity Certificate dialog box, enable Generate self-signed certificate and click Add Certificate.

**Caution**

At the Enrollment Status prompt, click OK

### STEP 13
In the Manage Identity Certificates dialog box, click OK.

### STEP 14
In the SSL VPN Wizard dialog box, click Next >.

## PART B: Configuring User Authentication, Creating and Testing the Group Policy
### STEP1
At the User Authentication step, select Authenticate using the local user database, and under User to be Added, in the Username text box, type (admin) and in the Password text box, type (uC@123456), and then in the Confirm Password text box, type (uC@123456), and then click Add >> then click Next>.

### STEP 2
At the Group Policy step, in the Create new group policy text box, type NY-Group-Policy and click Next >.

### STEP 3
At the Clientless Connections Only - Bookmark List step, click Next >.

**Caution**

At the No Bookmark selected prompt, click OK.

### STEP 4
At the Summary step, click Finish.

### STEP 5
Minimize the Cisco ASDM 7.3 for ASA - asa window.

### STEP 6
On the desktop, double-click the Google Chrome icon.

### STEP 7
In the address bar, type (https://192.168.1.207) and press Enter.

### ST5EP 8
On the Privacy error tab, click Advanced > Proceed to 192.168.1.207 (unsafe).

### STEP 9
On the SSL VPN Service tab, in the USERNAME text box, type admin and in the PASSWORD text box, type uC@123456, and then click Login.

### STEP 10
Close all windows.

**Caution**

If the Configuration Modified prompt appears, click Don't Save.

## LAB SUMMARY
Now, you are equipped with the knowledge and skills to configure clientless SSL VPNs on ASA. 

Submit your task, and after that, you can perform some additional tasks/activities given below:

>>View configured VPN connection profiles in ASDM.

>>Manage user accounts in the ASA local database.

>>Add bookmark lists for internal web applications.

## Disclaimer

This repository is for **educational and personal learning purposes only**.  

The original lab content belongs to **uCertify / Ancora Education** and remains their copyrighted material.  
This repository is not affiliated with, endorsed by, or sponsored by uCertify or Ancora Education.  

No copyright infringement is intended.  
Use of any tools or techniques mentioned here should only be performed in authorized, legal environments.
