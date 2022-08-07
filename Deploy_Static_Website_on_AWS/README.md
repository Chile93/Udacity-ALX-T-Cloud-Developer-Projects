**Deploy Static Website on AWS**

In this project, a static website was deployed to AWS using S3, CloudFront, and IAM.

The files included are: 

index.html - The Index document for the website.
/img - The background image file for the website.
/vendor - Bootssrap CSS framework, Font, and JavaScript libraries needed for the website to function.
/css - CSS files for the website.


**Steps to Deploying a Static Website(Chinedu's Travel Blog) on AWS**;

- Create an S3 bucket that is visible in the AWS Management console.

- Upload the the website files to the S3 bucket.

- Configure the S3 bucket to support *static website hosting*.

- The bucket should have **IAM bucket policy** that makes the contents publicly accessible.

- Configure the CloudFront to retrieve and distribute website files.

- The website should be accessible to anyone on the Internet via a web browser, and provid the CloudFront domain name URL and website-endpoint URL for the website.
