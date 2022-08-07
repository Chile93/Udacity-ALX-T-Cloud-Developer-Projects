## Access Website in Web Browser

Note - In the steps below, the exact domain name and the S3 URLs will be different in your case.

Open a web browser like Google Chrome, and paste the copied CloudFront domain name (such as, dgf7z6g067r6d.cloudfront.net) without appending /index.html at the end. The CloudFront domain name should show you the content of the default home-page, as shown below:

The figure above shows the page displayed at https://dgf7z6g067r6d.cloudfront.net

Access the website via website-endpoint, such as http://<bucket-name>.s3-website.us-east-2.amazonaws.com/.


Access the bucket object via its S3 object URL, such as, https://<bucket-name>.s3.amazonaws.com/index.html.

s

All three links: CloudFront domain name, S3 object URL, and website-endpoint will show you the same index.html content.

If we were not "hosting" the website on S3, we could have made the bucket private and host the content only through the CloudFront domain name. In such a case, we cannot access the private content using S3 object URL and website-endpoint.

Troubleshooting Tip
After completing the project instructions, if you are unable to view the website contents, refer to the following guide: I’m using an S3 website endpoint as the origin of my CloudFront distribution. Why am I getting 403 Access Denied errors?

Refer to this official tutorial Using a website endpoint as the origin, with anonymous (public) access allowed, and verify if you have used the correct domain for your distribution. It should essentially be the Static website hosting endpoint of the form <bucket-name>.s3-website-region.amazonaws.com.

Use the Static website hosting endpoint to create the distribution
Use the Static website hosting endpoint to create the distribution
