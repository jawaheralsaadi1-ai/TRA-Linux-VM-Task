# TRA Linux VM Task



\# \\ Linux VM Server Setup \& Java Application Deployment



This repository documents my training assignment where I built, configured, and deployed a remote Java application on an Ubuntu Server from scratch.



\---



\##  Server Specifications

\* \*\*Operating System:\*\* Ubuntu Server 22.04 LTS

\* \*\*Virtualization Platform:\*\* VirtualBox

\* \*\*Resources:\*\* 2 CPUs, 2048 MB RAM, 25 GB Storage



\---



\##  Task Execution Log



\###  Stage 1 \& 2: Remote Connection

\* Connected securely to the VM via SSH:

&#x20;   ```bash

&#x20;   ssh trainee@<VM-IP>

&#x20;   ```



\### 📍 Stage 3: Terminal Diagnostics

During this stage, I investigated system usage purely from the command line:

1\. \*\*Free Memory (RAM):\*\* Checked using `free -h`

2\. \*\*Disk Space on `/`:\*\* Checked using `df -h /`

3\. \*\*Kernel Version:\*\* Checked using `uname -r`

\*(Include screenshots of your results inside the `/docs` folder here!)\*



\### 📍 Stage 4 \& 5: Java \& App Deployment

\* \*\*Java Runtime installed:\*\* OpenJDK 17

\* \*\*Execution Command:\*\* ```bash

&#x20;   cd \~/apps \&\& java -jar yourproject.jar

&#x20;   ```

\* \*\*App Status:\*\* Successfully running and accessible from the host browser at `http://<VM-IP>:8080`.



\### 📍 Stage 6: Detached Running (Nohup)

\* To ensure the application survives terminal session termination, it was run in detached mode:

&#x20;   ```bash

&#x20;   nohup java -jar yourproject.jar > logs/app.log 2>\&1 \&

&#x20;   ```

\* \*\*Process Identification (PID):\*\* Managed via `ps aux | grep java`.



\---



\## 🧠 Key Takeaways

\* Learned how to manage headless Linux servers entirely via SSH.

\* Mastered conventional git workflows and neat file organization structures.

