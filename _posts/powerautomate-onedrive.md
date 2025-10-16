## I created a dedicated folder In OneDrive for my project. When I click on the Automate menu > Flows > I get "No flows available." Can I add a flow I created, to act on a file, in that folder, with a particular filename? Could it act on that file everytime I choose that flow? If so, how do I add a flow to the Automate > Flow menu for that OneDrive folder? Would it just appear in the menu for that folder?

Yes, you **can** create a Power Automate flow that acts on a file in a specific OneDrive folder, and you can **trigger it manually** from the **Automate > Flows** menu in OneDrive. However, there are a few key things to understand about how this works and how to make your flow appear in that menu.

---

### ✅ **What You Can Do**
You can:
- Create a **manual flow** (triggered by you) that acts on a file in a specific folder.
- Filter the flow to only act on files with a **specific filename** or pattern.
- Make the flow appear in the **Automate > Flows** menu when you right-click a file in OneDrive.

---

### 🛠️ **How to Set It Up**

#### 1. **Create the Flow**
1. Go to Power Automate.
2. Click **Create** > **Instant cloud flow**.
3. Choose **"For a selected file"** as the trigger (from **OneDrive for Business**).
4. Name your flow and click **Create**.

#### 2. **Configure the Trigger**
- The **"For a selected file"** trigger allows the flow to be manually run from the OneDrive interface.
- You can add **input fields** if needed (e.g., to confirm the filename or take user input).

#### 3. **Add Conditions (Optional)**
- Add a **Condition** action to check if the file name matches your target (e.g., `"filename.pdf"`).
- If it matches, proceed with your actions (e.g., move, rename, analyze, etc.).

#### 4. **Save the Flow**

---

### 📂 **How It Appears in OneDrive**

Once the flow is saved:
- Go to your **OneDrive folder** in the browser.
- Right-click a file or select it.
- Go to **Automate > Flows**.
- Your flow should now appear in the list **if**:
  - The flow uses the **"For a selected file"** trigger.
  - You have permission to run it.
  - The file is in **OneDrive for Business** (not personal OneDrive).

---

### 🔁 **Can It Act on the Same File Every Time?**
Yes, but:
- You must **select the file** each time you run the flow.
- The flow can check the filename and only proceed if it matches your criteria.

If you want it to run **automatically** whenever a file is added or modified, you’d need to use a **"When a file is created"** or **"modified"** trigger instead — but those won’t show up in the **manual Automate menu**.

---

Would you like help building a sample flow that checks for a specific filename and performs an action?

## It worked. When I tested it, I saw some unfamiliar flows. They look like other staff members flows. Can other people see my flow from their OneDrive? If so, how can I keep my flows private to my OneFolder?

Great to hear it worked! Regarding the unfamiliar flows you saw — here's what's likely happening and how to keep your flows private:

---

### 🔍 **Why You Might See Other People's Flows**
If you're seeing flows that you didn’t create, it could be due to one of these reasons:

1. **Shared Flows**: Someone may have shared a flow with you or with a group you're part of (like a Microsoft 365 Group or Team).
2. **Environment Settings**: If you're working in a **shared environment** (like a departmental or org-wide Power Platform environment), flows created there might be visible to others.
3. **Shared OneDrive Folder**: If the folder is shared with others, and the flow is tied to that folder, it might be visible to collaborators.

---

### 🔒 **How to Keep Your Flows Private**

To ensure your flows are **only visible to you**:

#### ✅ 1. **Use "My Flows"**
- When creating a flow, make sure you're in the **"My Flows"** section, not a shared team or environment.
- You can check this at the top of the Power Automate portal — it should say **"My flows"** and not a team or group name.

#### ✅ 2. **Don’t Share the Flow**
- Unless you explicitly **share** a flow or add co-owners, it should remain private.
- To check:
  - Go to **Power Automate** > **My Flows**.
  - Click the **three dots** next to your flow > **Manage run-only users**.
  - Make sure no one is listed unless you want them to be.

#### ✅ 3. **Avoid Shared Environments**
- If your organization uses custom environments (e.g., "TDI Projects" or "Web Team"), flows created there might be visible to others.
- Stick to the **default environment** unless you need to collaborate.

---

### 🧼 Want to Clean Up the Menu?
Unfortunately, you **can’t remove** other people’s flows from your **Automate > Flows** menu if they’ve been shared with you or are part of a shared environment. But you can:

- Ask the owner to **unshare** the flow if it’s not relevant to you.
- Create your flows in **your personal OneDrive** and **default environment** to keep them isolated.

---

Would you like help checking which environment your flow is in or how to move it to a private one if needed?
