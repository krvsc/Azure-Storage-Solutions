# Provide shared file storage for the company offices

This repository contains documentation for setting up file sharing for the company's geographically dispersed offices. The goal is to facilitate easy access to files while ensuring some content is accessible only from selected corporate virtual networks. Additionally, snapshots are configured for file protection and restoration.

## Architecture Diagram

![File Sharing Architecture Diagram](architecture_diagram.png)

## Skilling Tasks

1. Create a storage account specifically for file shares.
2. Configure a file share and directory.
3. Configure snapshots and practice restoring files.
4. Restrict access to a specific virtual network and subnet.

## Exercise Instructions

### 1. Create and Configure a Storage Account for Azure Files

- Open the Azure portal.
- Search for and select "Storage accounts".
- Click on "+ Create".
- Choose to create a new resource group and name it.
- Provide a unique name for the Storage account and set Performance to Premium.
- Choose Premium account type for File shares and set Redundancy to Zone-redundant storage.
- Review and create the storage account.
- Once deployed, navigate to the resource.

### 2. Create and Configure a File Share with Directory

- In the storage account, go to the Data storage section and select the File shares blade.
- Click on "+ File share" and provide a name.
- Accept the defaults and create the file share.
- Add a directory for the finance department and upload a file for testing.

### 3. Configure and Test Snapshots

- In the file share, navigate to the Snapshots blade.
- Create a snapshot for the file share.
- Practice restoring a file from the snapshot.

### 4. Configure Restricting Storage Access to Selected Virtual Networks

- Search for and select "Virtual networks".
- Create a new virtual network with a subnet.
- In the subnet settings, choose Microsoft.Storage in the Services drop-down under Service endpoints.
- Save your changes.
- In the file storage account, go to the Networking blade in the Security + networking section.
- Change Public network access to Enabled from selected virtual networks and IP addresses.
- Add the existing virtual network and subnet.
- Save your changes.

## Conclusion

Following these steps will result in the setup of a storage account for file sharing, with specific configurations for access restriction, snapshots, and directory organization. Access to files is facilitated while ensuring security measures are in place, such as restricting access to selected virtual networks. Additionally, snapshots provide protection against accidental deletion and enable easy file restoration when needed.