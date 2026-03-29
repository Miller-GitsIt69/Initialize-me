<h1>🖥Virtual Machine instance🖥</h1>

 ### [YouTube Demonstration] (Coming Soon!)

<h2>Description</h2>
- In this repo, I am simply showing the step-by-step process of generating a Virtual Machine instance on the Google Cloud Platform (GCP) console. 
  
   - FYI: A Virtual Machine (VM) instance is a software-based, emulated computer running on physical hardware, providing a fully isolated operating system environment. Instances are typically managed in the cloud to provide scalable computing, storage, and networking resources on-demand, often referred to as cloud instances or virtual servers. 
<br />


<h2>Languages and Utilities Used</h2>

- <b>GitBash Command Line Interface</b>
- <b>GitHub.com</b>
- <b>Google Cloud Console</b>
- <b>VSCode code editor</b>


<h2>Environments Used </h2>

- <b>Windows 11 Pro</b> (25H2)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

# GCP-Lab1
Created a VM instance, performed health, metadata &amp; validity checks

## Generating a VM instance:
> Navigate to and login to GCP Console

> Create VM (search "VM" in search bar, "Create VM" from products,  or select "Hamburger" icon -> Compute engine -> VM Instances)
  
> [Machine Configuration] tab: Region is us-central1 (Iowa) or Sao Paolo --> DEFAULT!!

> [OS and storage] tab: Make sure Debian OS (Linux platform) is the image type
  
> [Data Protection] tab: No Backups (This is a Lab ONLY...this is NOT for production!)

> [Networking] tab: Check "Allow HTTP traffic" only
 
> [Observability] & [Security] tabs: Leave ALONE!!
  
> [Advanced] tab: Paste the copied user script into "Automation" field

> Click "Create"

> VM Homepage should generate 👈 Screenshot (Deliverable)

## Instance Health and Metadata checks:
> From the "VM Instances" screen, look for the "Connect" tab of the desired instance

> Under the Connect tab, click on the "SSH" option to ssh into the VM

> At the pop-up, select "Authorize"

> Once the ssh portal populates, type in "curl -s localhost/healthz" to check instance health [Output = "Ok" ]

> Next, type in "curl -s localhost/metadata | jq ." to check instance metadata [Output = Shows instance data ]

## Instance validation (HW deliverables):
> While the instance is running, open Gitbash/Terminal (Run as Administrator)

> Navigate to an empty folder and create a new file named "gate_gcp_vm_http_ok.sh"

> From this point in the terminal, type "code ." to open VSCode

> In VSCode, navigate to the "gate_gcp_vm_http_ok.sh" and paste the appropriate script & save the file

> In the Google Console, copy the "External IP" of your instance

> Next, type in "Ctrl + J" to open VSCode's terminal interface and type "VM_IP=[copied External IP] ./gate_gcp_vm_http_ok.sh" & press Enter

> Lab 1 Gate Result should = PASS, along with 5 other checks 👈 Screenshot 

> "badge.txt" & "gate_result.json" files should generate within the directory/folder

>  Next, select the "gate_result.json" file 👈 Screenshot (Deliverable)

> Lastly, type in "cat badge.txt" [Output = "GREEN" ] 👈 Screenshot (Deliverable)


 ![](https://i.ytimg.com/vi/I1v0DZYcFeA/maxresdefault.jpg)

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
