# CW-Deploy

## Table of Contents 2

1. [Introduction](#introduction)
1. [Structure](#structure)
    1. [Structure Summary System Build](#summarysystembuild)
    1. [Structure Directory Tree](#directorytree)
        1. [Role Folders](#rolefolders)
        1. [Variable Folders](#varsfolders)
        1. [Miscellaneous Folders](#miscfolders)
1. [Roadmap](#roadmap)

<div id='introduction'/>

### **What's the idea of this project?** 💡

Set up and configure cloud instances automatically. This is powered by the automation tool Ansible which is co-developed by Red Hat among many other free developers. CW-Deploy works only on linux and is and was tested with Fedora (33) Server.

The repository of ansible is available on GitHub --> [Ansible](https://github.com/ansible/ansible)

---
<div id='structure'/>

### **Structure** 🏗️

As frontend [Apache](https://apache.org/) is needed and as backend [Nginx](https://nginx.org/en/) as proxy. So we have the best performance on the dashboard and also in the backend with the data processing which Nginx does. As cloud engine we use [Nextcloud](https://nextcloud.com/) which is also free and open source.

<div id='summarysystembuild'/>

#### **Structure Summary System Build** ✍️

- Frontend 🖥️
  - Apache
- Backend 📊
  - Nginx
- Cloudengine 🌩️
  - Nextcloud

<div id='directorytree'/>

#### **Structure Directory Tree** ✍️

The following directories are roles folders:

1. SYSTEM
1. CW-INSTALL
1. CONFIG

This is also the right order in which way they are replayed. All other folders or files are special config files.

| File/Folder                | Description                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------|
| ``ansible.cfg``            | Ansible's configuration file, we are defining here where the host file is or the plugin to load.    |
| ``cw-deploy-playbook.yml`` | Its the playbook file of this Project.\ Here we are defining which roles in which way are *played*. |
| ``.gitignore``             | Definition file from git to ignore files or folders who don't get pushed to the repository          |
| ``hosts``                  | Host file where you remote servers/hosts are defined                                                |
| ``README.md``              | That file which you actually read                                                                   |

---

<div id='rolefolders'/>

#### **Role Folders**

In every role folder, they have the same folder structure, as example here I took the ``CONFIG`` folder.

📦CONFIG\
 ┣ 📂defaults\
 ┃ ┗ 📜main.yml\
 ┣ 📂files\
 ┣ 📂handlers\
 ┃ ┗ 📜main.yml\
 ┣ 📂tasks\
 ┃ ┗ 📜main.yml\
 ┣ 📂templates
 ┗ 📂vars\
 ┃ ┗ 📜main.yml

<div id='varsfolder'/>

#### **Variable Folders**

This are the ``var`` folders/files in every role folder.

---

┣ 📂defaults\
 ┃ ┗ 📜main.yml\

---

┗ 📂vars\
 ┃ ┗ 📜main.yml

---

<div id='miscfolders'/>

#### **Miscellaneous Folders**

Additionally there is a plugin folder. In this folder I put the mitogen plugin. You can simply download this unzip and put it in the plugin folder. In the ansible.cfg this must be defined, where the plugin is and also that this should be used.

📦PLUGINS\
 ┣ 📂mitogen-0.2.9

> Keep in mind that your version can be different to mine.

---

<div id='roadmap'/>

### **Roadmap** 🛣️

| To-Do                                    | Achieved |
|------------------------------------------|:--------:|
| Automatic system updates                 | ✅       |
| Deactivate unused Services (ex. IPv6)    | ✅       |
| Autoremove deprecated packages           | ❌       |
| Installing Apache                        | ❌       |
| Installing Nginx                         | ❌       |
| Installing Nextcloud                     | ❌       |
| Configure Apache for Nextcloud (LOCAL)   | ❌       |
| Configure Apache for Nextcloud (EXTERN)  | ❌       |
| Configure Apache and Nextcloud for SSL   | ❌       |
| Setup Autorenew Service for SSL          | ❌       |
| Configure Nginx as proxy for the backend | ❌       |

---

> *This does not indicate the order in which it is done.This would be updated continuously*

---
