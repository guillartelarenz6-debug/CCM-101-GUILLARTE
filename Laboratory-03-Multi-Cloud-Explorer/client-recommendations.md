
# Client Recommendations & Multi-Cloud Decision Matrix

## Client Recommendations (Checkpoint 4)

### Client A – Startup Company
- **Recommended Platform:** Amazon Web Services (AWS)
- **Justification:** AWS provides an exceptional startup ecosystem, including generous cloud credits, rapid scaling capabilities, and minimal upfront infrastructure investment. As the startup grows, AWS's vast service catalog allows them to easily adopt advanced managed services without switching cloud providers.
- **Key Services to Use:** Amazon EC2 / AWS Fargate, Amazon DynamoDB, Amazon S3.

### Client B – University
- **Recommended Platform:** Microsoft Azure
- **Justification:** Since the university already relies heavily on Windows Server, Microsoft 365, and Active Directory, Microsoft Azure provides native identity federation via Microsoft Entra ID and seamless hybrid connectivity. This minimizes migration friction, optimizes licensing costs, and reduces operational overhead for IT staff.
- **Key Services to Use:** Microsoft Entra ID, Azure Virtual Machines, Azure SQL Database.

### Client C – AI Research Company
- **Recommended Platform:** Google Cloud Platform (GCP)
- **Justification:** GCP offers industry-leading AI and machine learning infrastructure powered by custom Tensor Processing Units (TPUs) and Vertex AI tools. It provides optimized high-performance computing clusters specifically designed to train complex deep learning models at scale.
- **Key Services to Use:** Google Vertex AI, Cloud GPUs/TPUs, Compute Engine (HPC nodes).

### Client D – Global E-Commerce Company
- **Recommended Platform:** Amazon Web Services (AWS)
- **Justification:** AWS offers the highest number of availability zones and edge locations globally, ensuring low latency and maximum uptime for international shoppers. Its mature auto-scaling features and global content delivery network allow it to handle sudden traffic surges smoothly during high-peak sales.
- **Key Services to Use:** Amazon CloudFront (CDN), AWS Auto Scaling, Amazon Aurora (Global Database).

---

## Multi-Cloud Decision Matrix (Checkpoint 6)

| Business Requirement | Recommended Platform | Justification |
| :--- | :--- | :--- |
| **Startup Company** | AWS | Offers generous startup credits, rapid serverless scaling, and quick time-to-market. |
| **Enterprise Organization** | AWS / Azure | Provides high compliance standards, global reach, and robust enterprise support contracts. |
| **Microsoft Environment** | Microsoft Azure | Delivers native hybrid identity sync with Active Directory and cost-effective Windows licensing. |
| **AI / Machine Learning** | Google Cloud Platform | Features advanced Vertex AI platforms, TPU chips, and native TensorFlow ecosystem support. |
| **Kubernetes Deployment** | Google Cloud Platform | GKE offers the most mature managed Kubernetes solution directly built by Kubernetes creators. |
| **Global Web Application** | AWS | Provides unmatched edge CDN locations (CloudFront) and robust auto-scaling infrastructure. |
