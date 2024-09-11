# 🚀 Configuring a RADIUS Server with Windows: Because Who Doesn't Love Authentication?

**Welcome to the thrilling world of RADIUS!** In this lab, I took on the mighty task of setting up a **Remote Authentication Dial-In User Service (RADIUS)** server on a Windows machine. I know what you're thinking: “What’s more exciting than configuring network policies?” Well, buckle up, because we’re about to get nerdy.

## 🛠️ What Did I Do?

1. **Added Network Policy Server Role**:  
   I kicked things off by giving Windows the superpower of **Network Policy Server (NPS)**. You know, because who doesn’t want to be in charge of all those authentication requests?
   
2. **Configured RADIUS Clients**:  
   Configured RADIUS clients to handle authentication like a boss. Set a shared secret (spoiler: it’s more secure than “password123” 😉), and now my Windows server is *trustworthy*.

3. **Created a Network Policy**:  
   🎯 Defined a custom network policy that says, “Hey, you from 192.168.1.100, you're good to go!”— granting access like the gatekeeper of the network.

4. **Registered the Server in Active Directory**:  
   🏢 Made sure my server was a certified member of the Active Directory cool kids club by registering it there.

## 🧰 Tools of the Trade:

- **Windows Server 2012 R2**: Because even servers deserve a little flair.
- **Network Policy Server (NPS)**: The brains behind RADIUS—think of it as the ultimate bouncer for network access.
- **Shared Secrets**: Because we all have secrets… some are just better encrypted than others.

## 😎 Why It’s Important:

Setting up a RADIUS server ensures that your network has **secure, centralized authentication** for users trying to gain access. So instead of passwords flying around everywhere like confetti at a party, everything is organized, secure, and (most importantly) manageable. 🎉

---

⚡ **Pro-tip**: If you want to feel like the ultimate network overlord, nothing beats managing authentication policies from a single, powerful server. Plus, it’s way more fun than it sounds. 😏

---
## 👉🏾 [Lab Walkthrough](https://github.com/Kpierre03/RADIUS/blob/main/RADIUS.md)
Let me know if you have any questions—just don’t ask for my shared secret! 🔒
