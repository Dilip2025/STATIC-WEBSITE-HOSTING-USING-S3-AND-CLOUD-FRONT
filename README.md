# STATIC-WEBSITE-HOSTING-USING-S3-AND-CLOUD-FRONT
![sc-1](https://github.com/user-attachments/assets/8aceefc7-3ef4-44f4-a173-63a8675e1033)



























This project demonstrates the implementation of a scalable, cost-effective, and highly available static website hosting solution using Amazon S3 and Amazon CloudFront. By leveraging AWS services, the website ensures fast and secure content delivery to users globally, with minimal infrastructure management

**Key Features:**
Amazon S3: Used to host the static website files (HTML, CSS, JavaScript, and images) in a cost-effective and scalable way. S3 offers high availability and durability, ensuring your website is always accessible.
Amazon CloudFront: Configured as a content delivery network (CDN) to distribute the website’s content globally. It speeds up delivery by caching content at edge locations close to the user, reducing latency and improving website performance.
Version Control: With S3 versioning, older versions of files are retained for backup and quick recovery in case of accidental overwrites or deletions.

**How It Works:**
Website Hosting: The static content (HTML, CSS, JavaScript, images) is uploaded to an S3 bucket. The bucket is configured for public access and static website hosting.
Global Distribution: CloudFront is set up to pull content from the S3 bucket and distribute it via its global edge locations. This ensures fast delivery and reduces latency for users regardless of their geographic location.
Content Delivery: CloudFront automatically caches website content at edge locations, optimizing performance by reducing load times for users around the globe.

**AWS Services Used:**
Amazon S3: Storage for static website files.
Amazon CloudFront: Content delivery and caching for improved performance and security.

**Project Files:**
Website source code (HTML, CSS, JavaScript)
S3 bucket configuration details
CloudFront distribution setup and configuration

**Benefits:**
Scalability: Easily scales to accommodate traffic spikes without additional infrastructure.
Cost-Effective: Pay only for the storage and bandwidth you use, with no need for servers or complex infrastructure management.
High Availability: AWS ensures the website is available with 99.99% uptime.
Performance: CloudFront accelerates content delivery by using edge locations for caching.
