the cmd

ansible-galaxy init devops_tools

![image](https://github.com/user-attachments/assets/073a141e-719c-4c12-b425-b3313482f33d)

cd devops_tools

![image](https://github.com/user-attachments/assets/ba10744b-2044-4c34-a5fc-9a4b256ffce2)

Come to the home

Cd /home 

![image](https://github.com/user-attachments/assets/9da2cf4f-cebd-4ea5-b4ce-400fb64bbbe7)

----------------------------------------------------
Vi site.yml
---
- name: Setup DevOps Tools (Git, Docker, Jenkins)
  hosts: all
  become: yes

  roles:
    - devops_tools
---------------------------
Then run the playbook
Ansible-playbook site.yml


Install Prometheus & Grafana using Ansible

🔧 Prometheus Setup
📁 Step 1: Create a directory (name it as you like)
---------------------------------------------------
mkdir prometheus
cd prometheus
--------------------------------
📄 Step 2: Copy the prometheus_install.yml playbook into this folder
-------------------------------
▶️ Step 3: Run the playbook
ansible-playbook prometheus_install.yml
-----------------------------------
This will install and start Prometheus automatically.
--------------------------------------
🌐 Step 4: Access Prometheus
Open your browser
Go to:
http://<your-public-ip>:9090
-----------------------------------------
You should now see the Prometheus web UI.
![Image](https://github.com/user-attachments/assets/3a071f71-bb61-425b-80eb-bb36de96426e)
------------------------------------------------
![Image](https://github.com/user-attachments/assets/7cab160b-0b7c-442a-9e31-c4a4ba5ebaed)

🎨 Grafana Setup
📁 Step 1: Create a directory (name it as you wish)
mkdir grafana
cd grafana
-------------------------------------------
📄 Step 2: Copy the grafana_install.yml playbook into this folder
-----------------------------------------------
ansible-playbook grafana_install.yml
-----------------------------------------
🌐 Step 4: Access Grafana in your browser
Open your browser
http://<your-public-ip>:3000
--------------------------------------------
![Image](https://github.com/user-attachments/assets/3617b33f-fa92-4bed-b348-58a150b70b1b)
--------------------------------------------
![Image](https://github.com/user-attachments/assets/50dc04e6-bee3-4aa7-a320-bf03be129261)

--------------------------------------
✅ AWS Security Group Configuration

Make sure you allow the following inbound ports in your EC2 security group:
-----------------------------------------------------------------------

-----------------------------------------------------------------------
22	  SSH	          TCP	                  For Ansible to connect via SSH
----------------------------------------------------------------------
9090	Prometheus	  TCP	                 To access Prometheus UI
-----------------------------------------------------------------------
3000	Grafana	      TCP	                  To access Grafana dashboard
-----------------------------------------------------------------------------






