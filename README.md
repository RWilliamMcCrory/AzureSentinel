<h1>Azure Sentinel Tutorial MAP with LIVE CYBER ATTACKS!</h1>


<h2>Description</h2>
In this project, I setup Azure Sentinel (SIEM) and connect it to a live virtual machine acting as a honey pot. We will observe live attacks (RDP Brute Force) from all around the world. We will use a custom PowerShell script to look up the attackers Geolocation information and plot it on the Azure Sentinel Map! 
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Azure</b>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<h2>Project walk-through:</h2>


<p align="center">
Creating the Azure VM for the Honeypot
: <br/>

![image](https://user-images.githubusercontent.com/120264673/207056400-b39f39c6-d43a-46ac-b0d5-c1431fde0a9f.png)

<p align="center">
Setting custom inbound  security rule to allow all traffic
<br/>

![image](https://user-images.githubusercontent.com/120264673/207057330-02d2f506-a2ac-497b-a872-2e3e5dc2d563.png)
<br />
<br />
<p align="center">
Setting up Log Analytics Workplace to ingest logs from the Honeypot VM
<br/>
</p>

![image](https://user-images.githubusercontent.com/120264673/207057918-1b33c4d6-8467-425a-bc73-4e13eb5361f5.png)


<p align="center">
Enabling Microsoft Defender for the server
<br/>

![image](https://user-images.githubusercontent.com/120264673/207058132-db30a6d1-28f7-43ed-97f9-3cf5db73148a.png)



<p align="center">
Configuring Microsoft Defender for Cloud to collect all events

<br/>

![image](https://user-images.githubusercontent.com/120264673/207058289-435f97c5-24e3-4583-af19-c6fbc12b1689.png)





<p align= "center">
Connecting Log Analytics workspaces to the Honeypot VM



![image](https://user-images.githubusercontent.com/120264673/207058634-b9186543-d84d-4d8d-8cde-023ab98d1517.png)


<p align= "center">
Adding Azure Sentinel (SIEM) to LAW

![image](https://user-images.githubusercontent.com/120264673/207059001-226d6786-a9c9-4dda-9760-11339684a89f.png)


<p align= "center">
Connecting to the VM and running a Powershell script to gather geo data from attackers

![image](https://user-images.githubusercontent.com/120264673/207059335-d7ba6e7a-6834-4785-b7c4-b46ed0900999.png)

![image](https://user-images.githubusercontent.com/120264673/207059372-061b8420-5c4c-4eb4-904d-6dc22b180826.png)

<p align= "center">
Creating custom log in LAW to bring in our log with the geo data

![image](https://user-images.githubusercontent.com/120264673/207059689-bd6d9ff2-e92c-435e-85dd-22c575237899.png)


<p align= "center">
Running query to see the failed login attempts with geo data from the attackers

![image](https://user-images.githubusercontent.com/120264673/207059895-b26d381e-0564-45fc-b512-5842b8681f80.png)


<p align= "center">
Extracting raw data and setting up custom fields

![image](https://user-images.githubusercontent.com/120264673/207060048-1cf0184a-e460-4b6e-8dbf-55eb6180add0.png)

<p align= "center">
Modifying some highlighted areas to improve the algorithm


![image](https://user-images.githubusercontent.com/120264673/207060175-918eab55-e1d1-42f0-930b-0d0098198156.png)

<p align= "center">
Using the query with Azure Sentinel to provide a visual of the attacks


![image](https://user-images.githubusercontent.com/120264673/207060560-cfe27de2-02d3-49e5-898e-117731164ec1.png)


<p align= "center">
Visual of the failed login attempts through Sentinel

![image](https://user-images.githubusercontent.com/120264673/207060816-8b7c0ef9-8643-4dd1-ba6d-402ac57c3103.png)





<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
