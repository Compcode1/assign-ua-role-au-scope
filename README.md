# Assign User Administrator Role at Administrative Unit (AU) Scope

This micro-project simulates assigning the **User Administrator** role scoped to a specific **Administrative Unit (AU)** in Microsoft Entra ID. It reinforces key principles of delegated identity management, scope limitation, and governance hygiene as defined by the Entra Control Stack model.

## 🧭 Scenario

We need to delegate user management responsibilities for the **Marketing Department** without granting tenant-wide administrative privileges. To do this, we’ll scope the **User Administrator** role to the **Marketing AU**, ensuring localized control and minimizing risk of over-privilege.

## 🔧 Step-by-Step Action Flow (Simulated)

- Navigate to **Microsoft Entra Admin Center** → **Identity** → **Administrative Units**
- Select or create the **Marketing AU**
- Add a user (e.g., `julia_admin@contoso.com`) to the AU
- Go to **Roles and administrators**
- Assign the **User Administrator** role, scoped specifically to the **Marketing AU**
- Confirm that `julia_admin@contoso.com` appears under role assignments for that AU

## 🔐 Entra Control Stack Mapping

| Layer | Description |
|-------|-------------|
| **Layer 1 – Authority Definition** | ✅ Confirmed via Global Admin or Privileged Role Admin initiating the scoped role assignment |
| **Layer 2 – Scope Boundaries** | ✅ Primary control layer. AU used to limit the scope of User Administrator privileges |
| **Layer 3 – Test Identity Validation** | ✅ Confirm `julia_admin` can manage users within the AU but cannot access users outside it |
| **Layer 4 – External Entry Controls** | ❌ Not affected. This scenario deals with internal delegation |
| **Layer 5 – Privilege Channels** | ✅ Scoped role assignment is a governed privilege channel |
| **Layer 6 – Device Trust Enforcement** | ❌ Not impacted. No Conditional Access or device policy applied in this simulation |
| **Layer 7 – Continuous Verification** | ✅ Role assignment should be periodically reviewed via Access Reviews and audit logs |

## 📌 Observations and Best Practices

- Scoped roles via Administrative Units provide granular control over identity management tasks
- Role assignment should always be documented and reviewed regularly
- Logging and Access Reviews should be configured to support visibility and audit compliance

## 📚 Part of the Entra Control Stack: Micro-Project Series

This project is part of a 5-part series designed to simulate real-world identity governance tasks within Microsoft Entra ID. Each project maps directly to the **seven-layer Entra Control Stack** to reinforce security architecture and operational integrity.

## ✅ Series Progress

- [x] Project 1 – Add a New Guest User  
- [x] Project 2 – Change a Global Administrator to a Privileged Role Administrator  
- [x] **Project 3 – Assign User Administrator Role at AU Scope** ← *This project*  
- [ ] Project 4 – Remove a Stale User Account  
- [ ] Project 5 – Create a Group and Assign Role

---

GitHub repo: https://github.com/CompCode1/assign-ua-role-au-scope
