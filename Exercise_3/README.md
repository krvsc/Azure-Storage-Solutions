# Provide private storage for internal company documents

This repository contains documentation for setting up storage solutions for the company's private documents and backing up the public website. The content is private to the company and shouldn’t be shared without consent. High availability and redundancy are crucial for this storage solution.

## Architecture Diagram

![Private Storage Diagram](architecture_diagram.png)

## Skilling Tasks

1. Create a storage account for the company's private documents.
2. Configure redundancy for the storage account.
3. Configure a shared access signature (SAS) for restricted access to a file.
4. Back up the public website storage.
5. Implement lifecycle management to move content to the cool tier.

## Exercise Instructions

**Note:** These instructions assume completion of exercise-2, Provide storage for internal documents.

### 1. Create a Storage Account and Configure High Availability

- Open the Azure portal.
- Search for and select "Storage accounts".
- Click on "+ Create".
- Choose the resource group created in the previous exercise.
- Set the Storage account name to "private" (ensure uniqueness).
- Review and create the storage account.
- Configure high availability:
  - In the storage account, go to the Data management section and select the Redundancy blade.
  - Ensure Geo-redundant storage (GRS) is selected.
  - Save your changes.

### 2. Create a Storage Container and Restrict Access to a File

- In the storage account, go to the Data storage section and select the Containers blade.
- Click on "+ Container".
- Name the container as "private".
- Set Public access level to Private (no anonymous access).
- Create the container.
- Upload a file to the private container for testing.
- Verify that the file is not publicly accessible.

### 3. Configure a Shared Access Signature (SAS)

- Select the uploaded blob file and move to the Generate SAS tab.
- Ensure the partner has only Read permissions.
- Set Start and expiry date/time for the next 24 hours.
- Generate SAS token and URL.
- Copy the Blob SAS URL to a new browser tab and verify access to the file.

### 4. Configure Storage Access Tiers and Content Replication

- Configure lifecycle management to move blobs from the hot tier to the cool tier after 30 days:
  - In the storage account, go to the Data management section and select the Lifecycle management blade.
  - Add a rule named "movetocool" to move blobs to cool storage after 30 days.
- Backup the public website files:
  - Create a new container called "backup" in the private storage account.
  - In the public website storage account, go to the Object replication blade.
  - Create replication rules to replicate files from the public container to the backup container in the private storage account.

## Conclusion

Following these steps will result in the setup of a storage account for the company's private documents with high availability and redundancy. Access to files can be restricted using shared access signatures, and lifecycle management ensures cost optimization by moving blobs to the cool tier after a specified period. Additionally, the public website files are backed up to another storage account for redundancy and disaster recovery purposes.