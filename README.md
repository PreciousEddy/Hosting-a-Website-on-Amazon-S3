# Hosting-a-Website-on-Amazon-S3

## Introducing Amazon S3!

### What it does & how it’s useful
Amazon S3 is a scalable object storage service used for storing and retrieving any amount of data from anywhere on the web. Developers and teams use Amazon S3 because of its scalability, durability, and security features.

### How I’m using it in today’s project
I’m using Amazon S3 in this project to host a static website, taking advantage of its reliable and scalable storage capabilities.

## Project Timeline
This project took me 2 hours to complete.
Documentation took me 30 minutes to write.

## File Directory

```python
project-root/
│
├── README.md
├── index.html
├── NextWork - Everyone should be in a job they love_files/
│   ├── style.css
│   ├── image.png
│   └── script.js
├── Images/
│   ├── s3-architecture.png
│   └── files.png
│   ├── Website.png
│   └── image.png
│   ├── static Hosting.png
└── errors/
        └── error-screenshot-1.png
```

## Create an S3 Bucket

### Creating an Amazon S3 bucket took me 10 minutes.

Some of the configuration steps include:

- **The bucket’s Region:** This specifies the geographical area where the bucket is created. I picked "US East (Ohio) us-east-2" for its proximity to my user base.
- **Access Control Lists (ACLs):** These define who can access the bucket and what actions they can perform. I set the ACL to allow public read access.
- **Bucket Versioning:** This keeps multiple versions of an object in the same bucket. I enabled versioning for data protection.
- **Public Access:** This setting controls whether objects in the bucket can be accessed publicly. I configured the bucket to allow public access for the website files.

S3 bucket names have to be globally unique, which means no two buckets can have the same name across all AWS accounts.

### My Created Bucket
I created a bucket named `nextwork-website-project-chibuik3`.

## Upload Website Files to S3
Next, I uploaded my website’s files into my S3 bucket.

There were two files to upload:
- `index.html`: The main HTML file that serves as the homepage.
- `NextWork - Everyone should be in a job they love_files`: The CSS file that styles the HTML content and some of the Js files.

These two files are related because the HTML file references the CSS file to apply the desired styling to the webpage.

## Static Web Hosting on S3

### Website Hosting
Website hosting means making your website accessible on the internet.

To enable website hosting, I:
1. Went to the S3 bucket properties.
2. Enabled static website hosting.
3. Specified `index.html` as the index document.

Once static website hosting is enabled, S3 produces a bucket endpoint URL. This URL allows users to access the hosted website.

## Diagrams
<div align="center">
    <p><strong>Setup Diagram:</strong></p>
    <img src="Images/files.png" alt="Setup Diagram" width="500">
</div>

<div align="center">
    <p><strong>Workflow Diagram:</strong></p>
    <img src="Images/s3-architecture.png" alt="Workflow Diagram" width="500">
</div>

## An Error!

When I visited the bucket endpoint URL, I saw a "403 Forbidden" error on my browser.

![Error Screenshot 1](error/error-screenshot-1.png)

The reason for this error was that the bucket policy was not configured to allow public access to the objects.

## My Key Learnings
- Setting up a static website on Amazon S3 is straightforward but requires careful attention to permissions and bucket policies.
- Ensuring public access settings are correctly configured is crucial for website accessibility.
- Versioning in S3 can help manage changes and provide data protection.

## Result🔥

<div align="center">
    <p><strong>Webiste Result:</strong></p>
    <img src="Images/Website.png" alt="Website" width="2000">
</div>