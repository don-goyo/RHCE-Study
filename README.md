# Project Name: RHCE Study

## 📌 Overview
Documentation on my preparation for RHCE exam objectives with Ansible; used Red Hat training and Sander van Vugt as primary learning resources.

## 🛠 Prerequisites
* **Ansible Core:** 2.16.19
* **Ansible-navigator** 26.6.0
* **Ansible-Automation-Platform** 2.6
* **Podman-image** registry.redhat.io/ansible-automation-platform-26/ee-supported-rhel9
* **Python:** 3.9.23
* **Collections:** `community.general 13.3.0`, `ansible.posix 2.2.2`, 'community.crypto 3.3.0', 'redhat.rhel_system_roles 1.120.6'
* **Target OS:** RHEL 9.7
* **Lab Environment:** VMware Fusion 13.6.1

## 📂 Project Structure
* 'inventory' example static inventory for lab
* 'ansible.cfg' example baseline ansible.cfg
* 'ansible-navigator.yml' example navigator config
* 'requirements.yml' Required collections for using example playbooks
* '/create-plays-playbooks' Practice with Jinja templates, loops and conditionals
* '/configure-managed-nodes' Setup and static IP address for new managed hosts
* '/automate-standard-rhcsa-tasks' Playbooks that manage default target, setup repository, setup storage and manage users and groups
* '/Practice_Exam' Complete Practice Exam example of covering the majority of the test objectives

## 🚀 Dependencies & Usage
1. Register control node with subscription-manager register
2. Run sudo dnf update to update RPM repositories
3. subscription-manager repos --enable ansible-automation-platform-2.6-for-rhel-9-aarch64-rpms
4. sudo dnf install ansible-navigator
5. Check ansible-navigator --version after installation; if receiving additional output besides listed version above install sqlite rpm package because it is missing.
6. podman login registry.redhat.io with credentials
7. podman pull registry.redhat.io/ansible-automation-platform-26/ee-supported-rhel9:latest
8. Setup baseline inventory, ansible.cfg and ansible-navigator.yml files
9. Install collections with ansible-galaxy collection install -r requirements.yml -p <your/custom/subdirectory>; I recommend practicing installing collections into custom subdirectory within your project directory so ansible-navigator can access the collections; if not, you will have to mount the default collections system locations in ansible-navigator.yml to access the collections
10. Check baseline config and inventory with ansible-navigator inventory and ansible-inventory --graph.
11. Check that collections installed correctly with ansible-galaxy collection list and note the locations

