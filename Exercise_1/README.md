# Provide storage for the IT department testing and training

This repository contains documentation for setting up storage solutions for the IT department's testing and training purposes. The content in this storage is meant for prototyping different storage scenarios and training new personnel. The configurations aim for simplicity and ease of change.

## Architecture Diagram

![Storage Account Diagram](architecture_diagram.png)

## Skilling Tasks

1. Create a storage account.
2. Configure basic settings for security and networking.

## Exercise Instructions

### 1. Create a Resource Group and a Storage Account

- Open the Azure portal.
- Search for and select "Resource groups".
- Click on "+ Create".
- Provide a name for the resource group (e.g., storagerg).
- Select a region.
- Review and create the resource group.

### 2. Create and Deploy a Storage Account

- Search for and select "Storage accounts".
- Click on "+ Create".
- Choose the previously created resource group.
- Provide a unique name for the storage account.
- Set the Performance to Standard.
- Review and create the storage account.
- Wait for the storage account to deploy and then go to the resource.

### 3. Configure Simple Settings in the Storage Account

- In the storage account, go to the Data management section and select the Redundancy blade.
- Select Locally-redundant storage (LRS) in the Redundancy drop-down.
- Save your changes.
- Ensure that only secure connections are allowed to the storage account:
  - In the Settings section, select the Configuration blade.
  - Enable Secure transfer required.
  - Set Minimal TLS version to Version 1.2.
  - Disable storage account key access:
    - Ensure Allow storage account key access is Disabled.
  - Save your changes.

### 4. Allow Public Access from All Networks

- In the Security + Networking section, select the Networking blade.
- Ensure Public network access is set to Enabled from all networks.
- Save your changes.

## Conclusion

Following these steps will result in the setup of a storage account for the IT department's testing and training purposes. The configuration ensures simplicity, low cost, secure transfer, and public access, making it suitable for prototyping different storage scenarios and training new personnel.