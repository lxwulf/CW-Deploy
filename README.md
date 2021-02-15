# CW-Deploy

## Table of Contents

1. [Introduction](#introduction)
2. [Structure](#structure)
    1. [Summary](#summary)
3. [Roadmap](#roadmap)

<div id='introduction'/>

### What's the idea of this project? 💡

Set up and configure cloud instances automatically. This is powered by the automation tool Ansible which is co-developed by Red Hat among many other free developers.

The repository is available on GitHub --> [Ansible](https://github.com/ansible/ansible)

---
<div id='structure'/>

### Structure 🏗️

As frontend [Apache](https://apache.org/) is needed and as backend [Nginx](https://nginx.org/en/) as proxy. So we have the best performance on the dashboard and also in the backend with the data processing which Nginx does. As cloud engine we use [Nextcloud](https://nextcloud.com/) which is also free and open source.

<div id='summary'/>

#### Summary ✍️

- Frontend 🖥️
  - Apache
- Backend 📊
  - Nginx
- Cloudengine 🌩️
  - Nextcloud

---

<div id='roadmap'/>

### Roadmap 🛣️

| To-Do                                    | Achieved |
|------------------------------------------|:--------:|
| Automatic system updates                 | ✅       |
| Autoremove deprecated packages           | ❌       |
| Installing Apache                        | ❌       |
| Configure Apache for Nextcloud (LOCAL)   | ❌       |
| Configure Apache for Nextcloud (EXTERN)  | ❌       |
| Configure Apache and Nextcloud for SSL   | ❌       |
| Setup Autorenew Service for SSL          | ❌       |
| Configure Nginx as proxy for the backend | ❌       |

---

> *This does not indicate the order in which it is done.*

---
