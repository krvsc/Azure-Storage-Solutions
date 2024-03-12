# Provide storage for the public website

This repository contains documentation for setting up storage solutions for the company's website. The content includes product images, videos, marketing literature, and customer success stories. It's essential to ensure low latency load times, keep track of document versions, and quickly restore documents if deleted.

## Architecture Diagram

![Storage Account Diagram](architecture_diagram.png)

## Skilling Tasks

1. Create a storage account with high availability.
2. Ensure the storage account has anonymous public access.
3. Create a blob storage container for the website documents.
4. Enable soft delete for easy restoration of files.
5. Enable blob versioning to keep track of document versions.

## Exercise Instructions

### 1. Create a Storage Account with High Availability

- Open the Azure portal.
- Search for and select "Storage accounts".
- Click on "+ Create".
- Choose a new resource group and provide a name.
- Set the Storage account name to publicwebsite (ensure uniqueness).
- Take default settings and review.
- Wait for deployment, then go to the resource.
- Enable Read-access Geo-redundant storage for high availability:
  - In the Data management section, select the Redundancy blade.
  - Ensure Read-access Geo-redundant storage is selected.

### 2. Ensure Anonymous Public Access

- In the storage account, go to the Settings section and select the Configuration blade.
- Enable the Allow blob anonymous access setting.

### 3. Create a Blob Storage Container

- In the storage account, go to the Data storage section and select the Containers blade.
- Click on "+ Container".
- Name the container as "public".
- Select Create.
- Configure anonymous read access for the public container blobs:
  - Select the public container.
  - On the Overview blade, select Change access level.
  - Set Public access level to Blob (anonymous read access for blobs only).
  - Select OK.

### 4. Configure Soft Delete

- Go to the Overview blade of the storage account.
- In the Properties page, locate the Blob service section.
- Ensure Enable soft delete for blobs is checked.
- Set Keep deleted blobs for (in days) setting to 21.
- Save your changes.
- Practice using soft delete to restore files:
  - Delete a file from the container.
  - Toggle Show deleted blobs.
  - Undelete the deleted file.

### 5. Configure Blob Versioning

- Go to the Overview blade of the storage account.
- In the Properties section, locate the Blob service section.
- Ensure Enable versioning for blobs checkbox is checked.
- Save your changes.
- Experiment with restoring previous blob versions:
  - Upload another version of the container file, overwriting the existing file.
  - Previous file versions are listed on the Show deleted blobs page.

## Conclusion

Following these steps will result in the setup of a storage account with high availability and anonymous public access for the company's website. Soft delete and blob versioning are enabled to ensure easy restoration of files and tracking of document versions, respectively.