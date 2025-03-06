# AWS S3 Static Website Hosting

📌 Project Overview
This project demonstrates how to **host a static website on AWS S3**, ensuring scalability, cost-efficiency, and ease of deployment. It includes a **three-page static website** with navigation, a footer, interactive UI elements, and a responsive design.

🚀 Features
- Static website hosted on **AWS S3**
- Secure **bucket permissions & access control**
- Step-by-step **configuration guide**
- **CloudFront integration** (optional) for faster content delivery
- **Route 53 domain management** (optional)
- SSL/TLS security for secure data transmission

📁 Project Structure
```
├── index.html      # Home Page
├── about.html      # About Page
├── contact.html    # Contact Page
├── assets/         # Images, CSS, JavaScript
└── README.md       # Documentation
```

🛠️ Deployment Steps
1️⃣ Create an S3 Bucket
- Log in to the **AWS Management Console**
- Navigate to **S3** and click **Create Bucket**
- Set a **unique name** and select a region
- **Uncheck** "Block all public access" to allow website hosting

2️⃣ Upload Website Files
- Open the S3 bucket
- Click **Upload** and add your **HTML, CSS, and assets**

3️⃣ Enable Static Website Hosting
- Go to **Properties** → **Static Website Hosting**
- Enable and set `index.html` as the default document
- (Optional) Set an error page (`error.html`)

4️⃣ Configure Public Access
- Go to **Permissions** → **Bucket Policy**
- Add the following JSON policy to allow public read access:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}
```

- Click **Save**

5️⃣ Access the Website
- Copy the **Bucket Website Endpoint** from the S3 settings
- Paste the URL into your browser

🌐 Optional Enhancements
- **CloudFront** for faster content delivery
- **Route 53** for custom domain setup
- **HTTPS (SSL/TLS)** for security

🎯 Conclusion
This project provides a practical guide to **deploying a static website on AWS S3** with best practices for security and performance optimization. 🚀
