# My Notes — Arinze Fortune Ihekweme

## Key Concepts I Learned
- **Azure Key Vault (AKV)** is the place where you can safely put away your "secrets", "keys" and "certificates" so they will be available for use by all of your cloud-based applications and services. 
- **your identity is the core of azure security**. So, it's very important that you have good Identity and Access Management (IAM) practices. IAM is the first layer of protection for azure. 
- **RBAC (role-based access control)** is the way microsoft recommends for managing permissions on your key vault. This is much better than the old ways of granting permission using legacy access policies because it provides a single point of administration and scalability. 
- **managed identities** provide a secure authentication process for azure services like App Service to Azure Key Vault, eliminating the need for your application to contain the credentials needed for this authentication. 
- **diagnostic logs** and **log Analytics** assist in monitoring, auditing, and investigating accesses to your Azure Key Vault resources.

  ---

## Lab / Hands-On Work

### What I did
Created **an Azure Key Vault**, in the **Azure Portal**.
Deployed **an Azure App Service (Web App)**.
Enabled **a System Assigned Managed Identity**, on the **App Service**.
Configured **Azure RBAC**, for the **Key Vault**.
Attempted to **create and manage secrets** in the **Key Vault**.
Used the Kudu (App Service Debug Console), to follow the mentor's example of **using PowerShell, to inspect the managed identity endpoint**.
Explored **diagnostic logging options**, as a method for monitoring **Key Vault Activity**.

### What happened / Result

I have been able to assign an identity with management to my App Service. 
I have also been able to go into the Kudu console and see that it is possible for your apps to be able to connect to other Azure Services using secure authentication instead of hard coding in your app's credentials. 
Also, through this lab I have seen how Role-Based Access Control (RBAC) works to control who has access to which resource of Azure Key Vault. 
This lab has shown me that the use of a Managed Identity removes the necessity of storing secrets within your application's code.

### Challenges I faced

I had problems with Authorization errors while trying to generate a new Secret in Azure Key Vault.
The problem arose because of lack of sufficient Azure Role Based Access Control (RBAC) permissions on my part.
In addition to learning about how long it takes for RBAC role assignments to be applied, I realized I needed to understand what was different regarding legacy Access Policies from Azure RBAC.

## My Takeaways

This session helped me understand that **Azure Key Vault is much more than a secret store—it is a critical security service that depends on strong identity and access management.**

The hands-on lab helped to emphasize the following key points:

- Fine grained authorizations can be implemented using Azure Role-Based Access Control (RBAC).
- For Password-less Authentication use Managed Identities in the Cloud.
- Protect identities by applying the principle of least privilege.
- Use Diagnostic logs and log analytics to monitor how access has been granted.

## Resources I Found Useful

- **Microsoft Learn – Azure Key Vault Documentation**  
  https://learn.microsoft.com/azure/key-vault/general/

- **Microsoft Learn – Azure RBAC Guide for Azure Key Vault**  
  https://learn.microsoft.com/azure/key-vault/general/rbac-guide

- **Microsoft Learn – Managed Identities for Azure Resources**  
  https://learn.microsoft.com/entra/identity/managed-identities-azure-resources/

- **Microsoft Learn – Monitor Azure Key Vault**  
  https://learn.microsoft.com/azure/key-vault/general/logging

- **Microsoft Learn – SC-500 Learning Path**  
  https://learn.microsoft.com/training/paths/sc-500-secure-azure-resources/

- **Microsoft Learn – Secure Azure Resources with Azure Key Vault Module**  
  https://learn.microsoft.com/training/modules/configure-and-manage-azure-key-vault/

- **Microsoft Cloud & AI Security Bootcamp 2026 (Session Recording)**  
  https://www.youtube.com/watch?v=GKqpej4X9B0&t=5936s
---

*Submitted by: **Arinze Ihekweme** ·
