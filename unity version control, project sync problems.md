# Unity Version Control Fix (Cloud Not Pulling Changes)

## Problem
### I was not able to properly sync my unity cloud project between my Desktop and my Laptop.
Unity Version Control (Plastic SCM) is connected, but:

- Pull does nothing  
- Cloud changes don’t appear  
- Project is out of sync  

This is usually caused by a **broken or desynced workspace connection**.

---

## What fixed it for me:

### 1. Open Unity Hub
- Locate your project  
- Click the **⋮ (three dots)** menu  

### 2. Disconnect Version Control
If available, click:

Disconnect from Unity Version Control


### 3. Force Project Refresh
- Open the project  
- Make a small change (e.g. move an object or edit a script)  
- Save  
- Close Unity  

### 4. Reconnect
- Go back to Unity Hub  
- Click **Connect to Unity Version Control**

### 5. Test
- Reopen the project  
- Try pulling changes again  

---

## If "Disconnect" is NOT visible

Unity Hub can be inconsistent.

### Check inside Unity:
- Open the project  
- Go to:

Window → Version Control

- Verify a workspace is assigned  

If things still seem broken → use the full reset below.

---

## Full Reset (Recommended if Quick Fix Fails)

### 1. Close Unity

### 2. Delete workspace data
In your project root, delete:

.plastic


### 3. Reopen the project
- Unity will detect no workspace  

### 4. Reconnect Version Control
- Re-link your cloud repository  
- Allow Unity to rebuild the workspace  

---

## What This Fixes

- Broken workspace state  
- Silent pull failures  
- Desynced local/cloud state  
- Invalid or stale connection  

---

## What This Does NOT Fix

- Merge conflicts  
- Missing or ignored files  
- Wrong repository selection  
- Permission/access issues  

---

## Explanation

Unity lost a valid workspace connection, preventing it from syncing with the cloud repository.  
Resetting or reconnecting rebuilds that connection.

---

## Pro Tip

If pull behaves strangely:

> Delete `.plastic` → reconnect → done

This is the fastest reliable fix for most connection-related issues.
