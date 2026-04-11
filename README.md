# Project Name: RHCE Study

## 📌 Overview
Practicing RHCE exam objectives with ansible

## 🛠 Prerequisites
* **Ansible Core:** 2.16.16
* **Python:** 3.9.25
* **Collections:** `community.general 12.5.0`, `ansible.posix 2.1.0`, 'redhat.rhel_system_roles 1.108.6'
* **Target OS:** RHEL 9.7
* **Lab Environment:** VMware Fusion 13.6.1

## 📂 Project Structure
Briefly explain the layout so other engineers can navigate it:
* `group_vars/`: Contains encrypted environment variables (Vault).
* `roles/`: Modular tasks for `common`, `webserver`, and `database`.

## 🚀 Usage
Provide the exact commands to run playbooks:

1. **Install Dependencies:**
   ansible-galaxy install -r requirements.yml
