
# Research: Types of Cloud Storage

## Cloud Storage Comparison

| Storage Type | Description (How it stores data) | Primary Use Case | Cloud Provider Example |
| :--- | :--- | :--- | :--- |
| **Block Storage** | Splits data into fixed-size blocks with unique identifiers. Acts like raw, unformatted hard drives attached to a server. | High-performance databases, virtual machine boot volumes, and operating systems. | AWS EBS (Elastic Block Store) |
| **File Storage** | Organizes data hierarchically in a shared folder structure using file paths and directories (like a traditional shared drive). | Centralized file sharing, content management systems, and legacy application storage. | AWS EFS (Elastic File System) |
| **Object Storage** | Stores data as discrete objects containing raw payload data, customizable metadata, and a unique identifier within a flat namespace. | Unstructured media files (images, videos), backups, logs, and big data storage. | AWS S3 / MinIO |

---

## Client Recommendation

Object Storage is the ideal choice for storing millions of user-uploaded images because it utilizes a flat, highly scalable namespace rather than a restrictive file-system hierarchy. Unlike block storage, which has fixed capacity limits, object storage scales virtually endlessly without complex drive partitioning or management. Additionally, object storage allows us to attach custom metadata directly to each photo, enabling efficient indexing, fast retrieval, and direct serving via web application APIs.
