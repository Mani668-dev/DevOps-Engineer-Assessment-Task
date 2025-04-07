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
mkdir prometheus
cd prometheus
📄 Step 2: Copy the prometheus_install.yml playbook into this folder
▶️ Step 3: Run the playbook
ansible-playbook prometheus_install.yml
This will install and start Prometheus automatically.
🌐 Step 4: Access Prometheus
Open your browser
Go to:
http://<your-public-ip>:9090
You should now see the Prometheus web UI.
![image](C:\Users\mani0\OneDrive\Pictures\promthous.jpg)
