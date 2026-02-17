# App Service Deployment Slots + Autoscale + Backup (Standard Tier)

This repository supports my lab walkthrough video on managing **Azure App Service** using **deployment slots**, **swap/rollback**, **autoscale**, and **backup configuration** 

📺 **Watch the lab video on YouTube:** https://youtu.be/clmnaOe7AzQ
---

## 🔍 Lab Overview

In this lab, you’ll learn how to:

- Create an App Service Plan (Standard tier) and Web App
- Create a **deployment slot** (`staging`)
- Perform a **slot swap** for zero-downtime deployment
- Execute a **rollback** by swapping back
- Configure **autoscale** rules (CPU or schedule)
- Configure **App Service backups** to an Azure Storage account

These tasks are frequently tested on AZ-104 and commonly used in production environments.

---

## 🧪 Lab Scenario

Your organization needs safer deployments with minimal downtime and a rollback strategy. You will use deployment slots for staged releases, autoscale the platform to handle load, and configure backups for operational recovery.

---

## 🛠️ Key Tasks

✅ **Task 1: Create App Service Plan + Web App (Standard)**
- Create resource group: `rg-appsvc-slots-lab`
- Create an App Service plan (example: **Standard S1**)
- Create a Web App in the plan

✅ **Task 2: Create a Staging Slot**
- Create a deployment slot named `staging`
- Browse both production and staging URLs

✅ **Task 3: Swap Slots + Rollback**
- Swap `staging` → `production`
- Confirm production changes
- Roll back by swapping back

✅ **Task 4: Configure Autoscale**
- On the App Service plan, configure autoscale:
  - Example: scale out when CPU > 70%
  - Set min/max instance limits

✅ **Task 5: Configure Backups**
- Create (or select) a Storage account + container
- Configure App Service backup schedule
- Run **Backup Now** once

✅ **Task 6: Cleanup**
- Delete `rg-appsvc-slots-lab` after the lab (Standard tier costs money)

---

## 📁 Suggested Files

- `lab-guide.md`: Step-by-step portal instructions  
- `screenshots/`: Slot creation, swap, autoscale settings, backup configuration  
- `notes.md` (optional): Slot swap rules + autoscale vs scale up notes

---

## 🔗 Learn More

- [Deploy staging slots in App Service](https://learn.microsoft.com/azure/app-service/deploy-staging-slots)
- [Scale an App Service app](https://learn.microsoft.com/azure/app-service/manage-scale-up)
- [Set up autoscale in Azure](https://learn.microsoft.com/azure/azure-monitor/autoscale/autoscale-get-started)
- [Back up and restore App Service](https://learn.microsoft.com/azure/app-service/manage-backup)

---

## 🧵 Tags

`#Azure` `#AppService` `#DeploymentSlots` `#Autoscale` `#Backup` `#AZ104` `#AzureLabs`

Created by: **Zion Spearman**  
Use and modify this lab freely for study and practice.
