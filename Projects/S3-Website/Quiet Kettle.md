# Project: Static Website Hosting on Amazon S3

This repository documents the successful deployment of a static website using Amazon S3. The following steps were completed to configure the environment and host the site.

---

## Step 1: Created the S3 Bucket
I created a new S3 bucket within the **AWS Management Console**. I assigned the globally unique name **The-Quiet-Kettle** and selected the optimal AWS Region. To prepare for public access, I specifically disabled the **Block all public access** settings and acknowledged the configuration.

![Screenshot: Bucket Creation]()

---

## Step 2: Enabled Static Website Hosting
Inside the bucket properties, I activated the **Static website hosting** feature. I designated `index.html` as the default index document, which generated the unique Amazon S3 website endpoint for the project.

![Screenshot: Hosting Configuration]()

---

## Step 3: Configured Public Permissions
To allow visitors to view the site, I updated the **Bucket Policy** under the Permissions tab. I applied the following JSON policy to grant public read access:

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::The-Quiet-Kettle/*"
        }
    ]
}

---

## Step 4: Uploaded Website Assets
I uploaded the website's core files, including the `index.html` file and supporting assets, directly to the root of the S3 bucket. I verified that the file structure remained intact to ensure proper routing and asset loading.

![Screenshot: File Upload]()

---

## Step 5: Verified Deployment
Finally, I tested the deployment by navigating to the **Bucket website endpoint**. The site successfully resolved in the browser, confirming that the routing, permissions, and file structures were correctly configured.

![Screenshot: Final Website]()

---

## Technical Summary
* **Storage Platform:** Amazon S3
* **Bucket Name:** The-Quiet-Kettle
* **Access Level:** Public Read-Only
* **Delivery Method:** S3 Static Website Endpoint
