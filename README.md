# AWS S3 Web Traffic Monitoring System

This project demonstrates a secure static website hosted on AWS S3 with IAM role-based access control, CloudFront distribution, CloudTrail logging, and traffic monitoring to detect unauthorized activities and security threats such as potential DDoS attacks.

---

## Features

- **Static Website Hosting** on AWS S3 with role-based access control.
- **IAM Roles & Policies** to restrict and manage access for users and admins.
- **CloudFront CDN** configured for faster content delivery with logging enabled.
- **CloudTrail Logging** to monitor API calls and user activity for audit and threat detection.
- **Traffic Monitoring** with CloudWatch and Amazon Athena to analyze logs, detect anomalies, and trigger alerts.

---

## Project Walkthrough

### 1. IAM Users Setup

- **1-users.png:** Overview of IAM users created for this project, including an admin user and regular users.  
  ![IAM Users Overview](images/1-users.png)

- **2-user-role.png:** Detailed permissions attached to the standard user role defining their limited access.  
  ![User Role Permissions](images/2-user-role.png)

- **3-admin-role.png:** Permissions assigned to the admin role with full access to manage S3 buckets and CloudFront.  
  ![Admin Role Permissions](images/3-admin-role.png)

### 2. S3 Bucket Configuration

- **4-s3-bucket.png:** Main AWS S3 bucket configured to host the static website content.  
  ![S3 Bucket Setup](images/4-s3-bucket.png)

- **5-s3-objects-files.png:** Contents inside the S3 bucket including HTML, CSS, JS files, and other assets served by the site.  
  ![S3 Bucket Contents](images/5-s3-objects-files.png)

### 3. CloudFront Setup

- **6-cloud-front.png:** AWS CloudFront distribution setup as a CDN for the S3-hosted website to improve load times globally.  
  ![CloudFront Distribution](images/6-cloud-front.png)

- **7-cloud-front-logs.png:** Access logs collected by CloudFront capturing each request to the website.  
  ![CloudFront Logs](images/7-cloud-front-logs.png)

- **8-cloud-front-logview.png:** Visualization of CloudFront logs used to analyze traffic patterns and detect anomalies.  
  ![CloudFront Logs Analysis](images/8-cloud-front-logview.png)

### 4. Website and User Interfaces

- **9-s3-webpage.png:** Screenshot of the live static website hosted on S3 accessed via CloudFront.  
  ![Static Website](images/9-s3-webpage.png)

- **10-admin-login.png:** Admin login page interface to authenticate privileged users.  
  ![Admin Login Page](images/10-admin-login.png)

- **11-admin-manage-bucket.png:** Admin dashboard showing management capabilities over the S3 bucket contents.  
  ![Admin Dashboard](images/11-admin-manage-bucket.png)

- **13-user-login.png:** User login screen for regular users accessing protected resources.  
  ![User Login Page](images/13-user-login.png)

### 5. CloudTrail Logging and Security Monitoring

- **12-cloudtrail-setup.png:** Configuration screenshot of AWS CloudTrail capturing API activity for security auditing.  
  ![CloudTrail Setup](images/12-cloudtrail-setup.png)

- **15-login-logs.png:** CloudTrail logs capturing user activities including login attempts and bucket access.  
  ![Login Activity Logs](images/15-login-logs.png)

- **16-success-login.png:** Example of a successful login event recorded in the CloudTrail logs.  
  ![Successful Login Event](images/16-sucess-login.png)

- **17-unsuccess-login.png:** Failed login attempt captured, useful for identifying suspicious behavior.  
  ![Failed Login Event](images/17-unsucess-login.png)

### 6. Monitoring and Analysis Tools

- **18-cloud-watch.png:** CloudWatch dashboard set up to monitor key metrics and alarms for unusual activity or performance issues.  
  ![CloudWatch Dashboard](images/18-cloud-watch.png)

- **19-amazon-athena.png:** Amazon Athena interface used for querying CloudTrail and CloudFront logs to perform detailed security analysis and detect potential threats.  
  ![Amazon Athena Querying](images/19-amazon-athena.png)


---

## Summary

This system provides a comprehensive approach to secure static website hosting with real-time monitoring and logging of access and activities. By leveraging AWS IAM, CloudFront, CloudTrail, CloudWatch, and Athena, it offers robust visibility and control to reduce risk and enhance security posture.