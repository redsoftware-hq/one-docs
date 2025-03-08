# Installing OneLead

OneLead is an **open-source Frappe application** designed for lead management, integrating with **Meta (Facebook) Ads** and **Google Leads**. This guide provides step-by-step instructions for installing and setting up OneLead on a Frappe-based system.

---

## **1. Prerequisites**
Before installing OneLead, ensure the following requirements are met:

### **System Requirements**
- **Frappe Framework** (v15)
- **Bench CLI** installed

### **Meta Accounts**
- **Facebook Developer Account** ([Sign Up](https://developers.facebook.com/))

---

## **2. Installation Steps**

### **Step 1: Set Up a Frappe Site**
If you do not already have a running Frappe instance, install Frappe and create a new site:

```bash

# Create a new Bench directory
bench init --frappe-branch version-15 one-bench
cd one-bench

# Create a new Frappe site
bench get-app https://github.com/redsoftware-hq/onelead

bench --site mysite.local install-app onelead
```


