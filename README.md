<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Host a Website on Amazon S3

**Project Link:** [View Project](https://nextwork.ai/projects/70e2d059-31ab-5f67-8c58-f5edbd451140)

**Author:** saleh alkhawatrah  
**Email:** alkhawatas@gmail.com

---

![Image](https://nextwork.ai/charmed_amber_serene_ruru/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_5d4474f9)

## Introducing Today's Project!

### Project overview

In this project, I will demonstrate how to host a fully functional static website on the cloud using Amazon S3 . I'm doing this project to learn core cloud storage principles, how to manage public versus private bucket permissions, and how to configure static website hosting so web assets can be served live on the internet.

### Tools and concepts

Services I used were Amazon s3, Key concepts I learnt include bucket policies, uploading static website files, index.html, bucket endpoint URLs and ACLs and how they control access to the buckets objects.

### Time, challenges, and wins

This project took me approximately 1 hour. The most challenging part was creating the bucket policy. It was most rewarding to see the access denied error when I tried to delete the index.html file.

## How I Set Up an S3 Bucket

### What I did in this step

In this step, I will open the AWS Management Console and create an Amazon S3 storage bucket because S3 acts as the cloud foundation where all the static files for our website will be securely stored.

### How long it took to create the bucket

Creating an S3 bucket took me less than 5 minutes.
Since it was my first time there was a couple new concepts for me to learn

### Region selection

The region for my S3 bucket was automatically assigned to Europe (Stockholm) eu-north-1 by AWS, which is a close and efficient European region for my project deployment.

### Understanding bucket name uniqueness

S3 bucket names are globally unique! This means a name chosen by one user cannot be used by anyone else until that bucket is deleted.

![Image](https://nextwork.ai/charmed_amber_serene_ruru/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_ba6d42ad)

## Upload Website Files to S3

### What I did in this step

In this step, I will upload the website files into the s3 bucket,  this is important because it gives the bucket the content it needs to runn the website.

### Files I uploaded

I uploaded two files to my S3 bucket, the index.html file which will determine the structure of the website, and a folder of images and assets whicch will fill in the website.

### How the files work together

Both files are necessary for this project as the index.html file provides the structural code for the webpage, while the images and assets folder supplies the pictures and visual elements it needs to display correctly.

![Image](https://nextwork.ai/charmed_amber_serene_ruru/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_a265af88)

## Static Website Hosting on S3

### What I did in this step

In this step, I will make the website available on the interent, this is called static website hosting and this is important because without it the website files will stay as file and not turn into a website

### Understanding website hosting

Website hosting is a service that provides the physical storage space and technologies needed for a website to be viewed on the Internet.

### How I enabled website hosting

To enable website hosting with my S3 bucket, I clicked on the properties tab of my bucket and enabled static website hosting, and i labelled index.html as the index document

### Access Control Lists (ACLs)

An ACL is a set of rules that decides who can get access to a resource, and I enabled it.

![Image](https://nextwork.ai/charmed_amber_serene_ruru/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_c22c54c0)

## Bucket Endpoints

### Understanding bucket endpoint URLs

Once static website is enabled, S3 produces a bucket endpoint URL, which is a URL that takes me or anyone on the interent to the website that I'm hosting

### What I saw when I tested the endpoint

When I first visited the bucket endpoint URL, I ran into a 403 Forbidden error. Even though we turned off 'Block all public access', the individual files inside the bucket are still private by default. Because of this, we have to manually update their access settings to public so that anyone visiting the site can actually view the contents.

![Image](https://nextwork.ai/charmed_amber_serene_ruru/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_22ce4daf)

## Success!

### What I did in this step

In this step, I will go into the files I uploaded to the bucket and make them public as well, so that the website's contents can actually be viewed online.

### How I resolved the 403 error

To resolve this 403 Forbidden error, I updated the access settings of the files inside the bucket, usinf ACLs I made the bucket's files public. Once I checked the s3 bucket endpoint I can see the webpage successfully loaded up.

![Image](https://nextwork.ai/charmed_amber_serene_ruru/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_5d4474f9)

## Bucket Policies

### What I did in this extension

In this project extension I'm about to use bucket policies to control access to the bucket's files, I'm doing this so that I can stop people from deleting the objects inside the files.

### Understanding bucket policies

An alternative to ACLs are bucket policies, which are rules that determine who is allowed or not allowed to do something. The benefit of using bucket policies is that you can have have even greater control of the acces of the actions or of the action that people are or aren't allowed to do, while ACLs are useful for controlling public access to individual objects inside the bucket

![Image](https://nextwork.ai/charmed_amber_serene_ruru/uploads/70e2d059-31ab-5f67-8c58-f5edbd451140_sm2sm2sm)

### What my bucket policy does

My bucket policy denies everyone from delteing the idex.html file in the bucket, I tested this by trying to delete the index.html file and saw a permission denied error! this means the bucket policy worked, it successfully stopped me from deleting objects that I wanted to protect.

---

*Built with [NextWork](https://nextwork.ai) - [View this project](https://nextwork.ai/projects/70e2d059-31ab-5f67-8c58-f5edbd451140)*
