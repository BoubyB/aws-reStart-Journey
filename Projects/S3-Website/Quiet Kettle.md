
# Project: Static Website Hosting on Amazon S3

This repository documents the successful deployment of a static website using Amazon S3. The following steps were completed to configure the environment and host the site.

---

## Step 1: Created the S3 Bucket
I created a new S3 bucket within the **AWS Management Console**. I assigned the globally unique name **The-Quiet-Kettle** and selected the optimal AWS Region. To prepare for public access, I specifically disabled the **Block all public access** settings and acknowledged the configuration.

![Screenshot: Bucket Creation](PASTE_IMAGE_LINK_HERE)

---

## Step 2: Enabled Static Website Hosting
Inside the bucket properties, I activated the **Static website hosting** feature. I designated `index.html` as the default index document, which generated the unique Amazon S3 website endpoint for the project.

![Screenshot: Hosting Configuration](PASTE_IMAGE_LINK_HERE)

---

## Step 3: Configured Public Permissions
To allow visitors to view the site, I updated the **Bucket Policy** under the Permissions tab. I applied the following JSON policy to grant public read access:

```json
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
