# Deploying a Static Website to AWS S3 with HTTP using CloudFront.
![sc-1](https://github.com/user-attachments/assets/8aceefc7-3ef4-44f4-a173-63a8675e1033)

**By the end of this post you will be able to:**
Create an S3 bucket and Configure it for static website hosting.
Create a CloudFront distribution and link it with your custom domain.
Then Finally Link the CloudFront CDN and S3

**I have created a simple index.html file.**
![sc-2](https://github.com/user-attachments/assets/5ad82700-817b-49bd-be34-495d3d66ff45)

**index.html**

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SSB KART</title>
    <link rel="stylesheet" href="style.css">
    <script src="script.js"></script>
</head>
<body>
    <h1>welcome to SSB KART</h1>
    <button onclick="alert()">click</button><br><br>
    <a href="login.html">login</a><br><br>
    <a href="signup.html">signUp</a>
</body>
</html>

**webpage will look like this.**
![sc-3](https://github.com/user-attachments/assets/80ef79fe-eaf0-4335-8029-ad8533ca67ce)

**Open Amazon S3 in your aws console and click on Create bucket.**
![SCREENSHOT-1](https://github.com/user-attachments/assets/64972389-f50d-4e40-b9bb-f42930ebb155)

**Name your bucket it should be unique, so i am giving my domain name to s3 bucket.**
![SCREENSHOT-2](https://github.com/user-attachments/assets/e4f16cee-00dd-4b2f-a375-723104831122)

**In Block Public Access settings for this bucket, uncheck "Block all public access" and select the acknowledge at the end.**
![SCREENSHOT-3](https://github.com/user-attachments/assets/89ad0b57-ae45-4699-9e36-d010d83b9d1f)

**Rest of all settings are fine, click on create bucket at bottom.**
![SCREENSHOT-4](https://github.com/user-attachments/assets/90fb566f-40da-4cb5-8ddf-0d664562b017)

**Now go inside the s3 bucket and upload the web content you have.**
![SCREENSHOT-5](https://github.com/user-attachments/assets/1a8e01f4-88ef-4dfd-9ef5-7f92cac12265)
![SCREENSHOT-6](https://github.com/user-attachments/assets/e56e9705-79a9-45dc-acf7-ce50d2b53df4)
![SCREENSHOT-7](https://github.com/user-attachments/assets/a7380225-7583-431e-a35b-b29c7d430f74)

**Now go to "Properties" tab and enable "Static website hosting" enter index.html in index document section and save changes.**
![SCREENSHOT-8](https://github.com/user-attachments/assets/5ff2d7c0-a11d-4bb7-a289-66ee53af8307)
![SCREENSHOT-9](https://github.com/user-attachments/assets/ae36bbe4-8e1c-4b6a-ad27-eb8efb94928c)

**Now go to the Cloudfront to create a distribution**
![SCREENSHOT-11](https://github.com/user-attachments/assets/c5f7b1e8-e700-4028-a1e1-f8b214b62316)

**select the origin domain and hit the create distribution button**
![SCREENSHOT-12](https://github.com/user-attachments/assets/ee8cc079-d9de-41f7-951c-b39187d7bd9d)
![SCREENSHOT-13](https://github.com/user-attachments/assets/0ea029ca-85f2-463a-98ee-a92c687a19fe)

**Finally the cloudfront distribution domain created successfully and use the link to view the website**
![SCREENSHOT-14](https://github.com/user-attachments/assets/e9a05e67-2649-4ffc-bfa2-cd554f53211f)
![SCREENSHOT-15](https://github.com/user-attachments/assets/360985a2-9a20-483e-867b-27ae0eae0f22)

**We have successfully Deployed a Static Website to AWS S3 with HTTP using CloudFront.**

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
