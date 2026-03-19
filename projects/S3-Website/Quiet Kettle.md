# Hosting a Static Website on Amazon S3

This guide provides step-by-step instructions on how to configure an Amazon S3 bucket to host a static website. 

## Prerequisites
* An active AWS Account.
* A registered domain name (optional).
* Your website files (`index.html`, CSS, images).

---

## Step 1: Create an S3 Bucket
The first step is to create a bucket that will hold your website's content.

1. Sign in to the **AWS Management Console**.
2. Open the **Amazon S3 console**.
3. Choose **Create bucket**.
4. Enter a **Bucket name** (must be globally unique).
5. Under **Block Public Access settings**, uncheck **Block all public access**.
6. Acknowledge the warning and choose **Create bucket**.

[Image: S3 Bucket Creation]

---

## Step 2: Enable Static Website Hosting
1. In the **Buckets** list, select your bucket name.
2. Choose the **Properties** tab.
3. Scroll to **Static website hosting** and choose **Edit**.
4. Select **Enable**.
5. In **Index document**, enter `index.html`.
6. Choose **Save changes**.

[Image: Hosting Configuration]

---

## Step 3: Edit Permissions (Bucket Policy)
To make your website public, you must add a bucket policy.

1. Choose the **Permissions** tab.
2. Under **Bucket policy**, choose **Edit**.
3. Paste the following JSON:

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::your-bucket-name/*"
        }
    ]
}
