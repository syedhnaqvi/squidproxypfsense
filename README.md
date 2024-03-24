# # Setting up SQUID Proxy on Pfsenser Firewall - Lab
<img src="https://img.shields.io/badge/-pfSense%20Firewall-blue?style=for-the-badge"></img>

## Objective
This lab includes steps for setting up  squid proxy server on pfsense firewall in a VM for leanring and educational purpose .

### Skills Learned

- Install SQUID on pfsense
- Setup & Configure Squid

### Step -1
Sign in to pfsense console 912.168.1.1 username : admin Password pfsense
### Step -2
System > Package Manager > Available Packages
Search squid and Click Install then Confirm installtion process will take sometimw!
![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/d4e5e32e-7222-4cb1-b2ca-e502df50829b)

Once installed successfully will see this .
![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/e5dd4436-94c4-4615-b59f-11acefb032a5)

### Step -3
Go to Services>Squid Proxy Server
![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/771b6c74-96a0-48e6-a82e-bb80b9a45b32)

### Step -4
Setup Local Cache setting
![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/075d18d8-2d73-4636-bd61-70a88bbcb106)

Customzie Hard drive space recommdned not to allocate more than 90% of your hard drive size 
![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/480d3257-2c77-49eb-8199-3688ee40afbe)
<br>
Adjust Memeory Cache it will greatly enhance speed not to exceed 50T of your total memory.
![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/05660299-861c-42dd-8191-438fad4bc8ad)

Save when done.

### Step -5
Go to General settings and enable squid.
![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/4ee6c956-64dc-4c8d-a723-08a0cb9667bb)
SAVE Settings.

### Step -6
Add filerwall rule for LAN network.
![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/32cd7b9f-5bb0-46e1-a4b0-bd16176609f9)
![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/37f57fab-b152-4783-934b-9a1b40d751c4)

![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/5ffb4864-bbc4-4a90-9a26-2be3ab8fbd47)

![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/d349c694-383e-4753-820b-be736f15e2c7)

SAVE settings.Apply changes.

### Step -7
Setup Proxy on Win VM
Search proxy in search bar and then click .
![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/fda6a2d7-b2d9-433a-8540-996f0342eba6)

Enable proxy and give IP of pfsense and port configured in ealrier step. It will divert all windows traffic throuhg proxy.
![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/c021b5c8-ae49-4d7b-b60c-7b2b272204ca)
<br>
Can also setup proxy in chrome browser instead of applying system wide 
![image](https://github.com/syedhnaqvi/squidproxypfsense/assets/39069507/25e1bad6-b593-482a-8820-45a5d52faae9)

Enable Antivuris from Squid Proxy 
Go to Squud server settings enable Antivirus Set Clam AV update Every 1 hour and then Select nearest CAL AV region to your location Click SAVE.
Reboot Pfsense then you can manually update the AV. Diagnostics > Reboot






