# Provide storage for a new company app

This repository contains documentation for setting up storage for the company's new app. The goal is to ensure that storage is accessed securely using keys and managed identities. Role-based access control is implemented, and protected immutable storage is configured to assist with testing.

## Architecture Diagram

![Storage Setup Architecture Diagram](architecture_diagram.png)

## Skilling Tasks

1. Create the storage account and managed identity.
2. Secure access to the storage account with a key vault and key.
3. Configure the storage account to use the customer-managed key in the key vault.
4. Configure a time-based retention policy and an encryption scope.

## Exercise Instructions

### 1. Create and Configure a Storage Account and Managed Identity

- Navigate to the Azure portal.
- Search for and select "Storage accounts".
- Click on "+ Create".
- Create a new resource group and storage account with the necessary configurations.
- Once deployed, navigate to the storage account.
- Search for and select "Managed identities".
- Create a managed identity and assign the Storage Blob Data Reader role to it.

### 2. Secure Access to the Storage Account with a Key Vault and Key

- Assign Key Vault Administrator role to your user account.
- Create a new key vault and enable Soft-delete and Purge protection.
- Generate/import a key in the key vault.

### 3. Configure the Storage Account to Use the Customer Managed Key

- Assign the Key Vault Crypto Service Encryption User role to the managed identity.
- Navigate to the storage account and select the Encryption blade in the Security + networking section.
- Choose Customer-managed keys and select the key vault and key.
- Ensure the Identity type is User-assigned and select your managed identity.

### 4. Configure a Time-based Retention Policy and an Encryption Scope

- Create a container named "hold" in the storage account and upload a file.
- Set up a time-based retention policy for the container.
- Test the retention policy by attempting to delete the file.
- Configure an encryption scope with infrastructure encryption enabled.
- Apply the encryption scope to all blobs in a new container.

## Conclusion

Following these steps will result in the secure setup of storage for the company's new app, ensuring access is managed using keys and managed identities. Role-based access control is implemented, and protected immutable storage is configured for testing purposes. Additionally, time-based retention policies and encryption scopes are established to enhance security and compliance measures.