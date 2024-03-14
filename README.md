## Project: Comprehensive Azure Storage Solutions 

This repository contains detailed documentation for configuring Azure Storage solutions for various purposes, including IT department testing and training, public website hosting, private internal storage, shared file storage for company offices, and storage for a new company app. Each section provides step-by-step instructions along with explanations of why each configuration is necessary.

### Table of Contents
Exercise 1: Provide storage for the IT department testing and training <br>
Exercise 2: Provide storage for the public website <br>
Exercise 3: Provide private storage for internal company documents <br>
Exercise 4: Provide shared file storage for the company offices <br>
Exercise 5: Provide storage for a new company app <br>

---

### Exercise 1: Provide storage for the IT department testing and training

#### Objective:
To create a storage account for the IT department's testing and training purposes.

#### Instructions:
1. **Create a resource group**:
   - Go to the Azure portal.
   - Navigate to "Resource groups" and click on "+ Create".
   - Provide a name and select a region for the resource group.
   - Review and create the resource group.

2. **Create a storage account**:
   - Navigate to "Storage accounts" and click on "+ Create".
   - Choose the previously created resource group.
   - Provide a unique name for the storage account.
   - Set performance to Standard.
   - Review and create the storage account.

3. **Configure basic settings**:
   - Set redundancy to Locally-redundant storage (LRS) for cost-effectiveness.
   - Enable secure transfer required with TLS version 1.2.
   - Disable storage account key access.
   - Allow public network access from all networks.

#### Reasoning:
- **Resource Group**: Provides a logical grouping of resources for easier management and organization.
- **Storage Account**: Serves as the storage solution for testing and training data.
- **Basic Settings Configuration**: Optimizes the storage account for low-cost usage while ensuring secure transfer and access control.

---

### Exercise 2: Provide storage for the public website

#### Objective:
To create blob storage for hosting the public website with high availability and versioning.

#### Instructions:
1. **Create a storage account**:
   - Follow the steps provided in Exercise 1 but choose Geo-redundant storage (GRS) for high availability.

2. **Configure public access**:
   - Enable anonymous access to the blob storage.
   - Create a blob storage container with anonymous read access.

3. **Enable soft delete and blob versioning**:
   - Enable soft delete for 21 days.
   - Enable blob versioning to keep track of document versions.

#### Reasoning:
- **Storage Account Configuration**: Chooses GRS for high availability to ensure the website remains accessible even during regional outages.
- **Public Access Configuration**: Allows anonymous access to the website content for public viewing.
- **Data Protection Configuration**: Implements soft delete and blob versioning to protect against accidental deletion and maintain document versions.

---

### Exercise 3: Provide private storage for internal company documents

#### Objective:
To create private storage for internal company documents with high availability and shared access signature.

#### Instructions:
1. **Create a storage account**:
   - Follow the steps provided in Exercise 1 but choose Geo-redundant storage (GRS) for high availability.

2. **Create a private storage container**:
   - Create a container with private access.
   - Upload files for internal use.

3. **Configure shared access signature (SAS)**:
   - Generate SAS with read-only access for external partners.
   - Test access to ensure restricted permissions.

4. **Implement lifecycle management**:
   - Move blobs to the cool tier after 30 days for cost optimization.

#### Reasoning:
- **Storage Account Configuration**: Chooses GRS for high availability to ensure data accessibility.
- **Private Container Creation**: Ensures privacy and security by restricting access to internal company documents.
- **SAS Configuration**: Provides controlled access for external partners while maintaining data security.
- **Lifecycle Management**: Optimizes storage costs by moving less frequently accessed data to the cool tier.

---

### Exercise 4: Provide shared file storage for the company offices

#### Objective:
To create a storage account for shared file storage across company offices with snapshots and restricted access.

#### Instructions:
1. **Create a storage account**:
   - Create a premium storage account for Azure Files with zone-redundant storage.

2. **Configure file share and directory**:
   - Create a file share and directories for different departments.
   - Upload files and enable snapshots for data protection.

3. **Restrict access to specific virtual networks**:
   - Configure storage access from selected virtual networks only.

#### Reasoning:
- **Storage Account Configuration**: Chooses premium storage for optimal performance and reliability.
- **File Share Configuration**: Organizes data into directories for better management and enables snapshots for data protection.
- **Access Restriction Configuration**: Ensures data security by allowing access only from authorized virtual networks.

---

### Exercise 5: Provide storage for a new company app

#### Objective:
To create storage for a new company app with managed identities, key vault integration, and encryption.

#### Instructions:
1. **Create a storage account and managed identity**:
   - Follow the steps provided in Exercise 1.
   - Create a managed identity and assign appropriate permissions for access.

2. **Secure access with key vault and key**:
   - Create a key vault and key for storing access keys securely.

3. **Configure storage to use customer managed key**:
   - Integrate the storage account with the key vault and specify the managed key for encryption.

4. **Implement time-based retention policy and encryption scope**:
   - Configure time-based retention policy for immutable storage.
   - Create an encryption scope with infrastructure encryption enabled for enhanced security.

#### Reasoning:
- **Managed Identity Configuration**: Provides secure access to the storage account for the new company app.
- **Key Vault Integration**: Safely stores access keys and manages encryption keys.
- **Customer Managed Key Configuration**: Enhances security by using customer-managed keys for encryption.
- **Policy and Encryption Scope Implementation**: Ensures data integrity and confidentiality by enforcing retention policies and encryption at the infrastructure level.

---

By following the instructions provided in each exercise, you can effectively set up and configure Azure Storage solutions tailored to specific business requirements, ensuring secure, efficient, and scalable storage solutions.🤗
