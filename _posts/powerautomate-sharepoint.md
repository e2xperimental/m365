---
layout: post
title: Running Power Automate in SharePoint
date: 2025-10-17 15:45:00 -0500
category: Power Automate
---
## Can you create Flows in SharePoint?

Yes, you can create Power Automate flows in a SharePoint site. It’s a great way to automate tasks like approvals, notifications, or data collection. Here’s how it works:

---

### ✅ **What You Need**
1. **Access to the SharePoint site** (with at least *Edit* permissions).
2. A **Microsoft 365 license** that includes Power Automate.
3. The SharePoint site must be part of a **Microsoft 365 Group** (which most modern team sites are).

---

### 🔧 **Ways to Create Flows for SharePoint**
You can create flows directly from:
- **Power Automate portal**: https://make.powerautomate.com
- **SharePoint list or library**: Go to the list → click **Automate** → **Power Automate** → **Create a flow**.

---

### 🔁 **Common Flow Scenarios in SharePoint**
- **When a new item is added** → send an email or Teams notification.
- **Approval workflows** for documents or list items.
- **Move/copy files** between libraries or sites.
- **Trigger flows from buttons** in SharePoint using Power Apps or manually.

---

### ⚠️ Things to Watch Out For
- **Flows are tied to your account** unless you use a **service account** or **shared flow** via a solution.
- If you leave the org or lose access, your flows may stop unless ownership is transferred.
- For **team-wide flows**, consider using **Solutions** in Power Automate to package and share flows more robustly.

## How do you build a team-wide flow using Solutions?

Great question, Erik! Building a **team-wide flow using Power Automate Solutions** is the best way to ensure your flows are **shared, managed, and owned at the team or org level**, not just tied to your personal account.

Here’s a step-by-step guide to help you get started:

---

## 🧰 **What is a Solution in Power Automate?**
A **Solution** is a container for Power Platform components like flows, apps, tables, and connections. It allows you to:
- Share ownership and maintenance.
- Move flows between environments (e.g., dev → test → prod).
- Use **service accounts** or **environment-level connections**.

---

## 🛠️ **How to Build a Team-Wide Flow Using a Solution**

### 1. **Go to the Power Automate Portal**
- Navigate to https://make.powerautomate.com
- In the left menu, click **Solutions**.

### 2. **Create a New Solution**
- Click **+ New solution**
- Give it a name (e.g., `TDI SharePoint Automations`)
- Choose your **environment** (use a shared or team environment if available)
- Click **Create**

### 3. **Open the Solution and Add a Flow**
- Open your new solution
- Click **+ New → Flow**
- Choose the type of flow (e.g., Automated cloud flow)
- Build your flow as usual (e.g., trigger: *When an item is created in SharePoint*)

### 4. **Use Shared or Service Connections**
- When adding connectors (e.g., SharePoint, Outlook), **use a shared connection** or **service account** if possible.
- This ensures the flow doesn’t break if your personal account changes.

### 5. **Share the Flow with Your Team**
- After saving the flow, go to the **flow details**
- Click **Share**
- Add your team members or a security group
- They’ll be able to **edit, manage, or monitor** the flow depending on permissions

---

## ✅ **Best Practices**
- **Use environment variables** for URLs, email addresses, etc., to make flows portable.
- **Document** what the flow does and who owns it.
- **Test** in a dev environment before deploying to production.
