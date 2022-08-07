## Upload files to S3 Bucket

Once the bucket is open to its contents, click the “Upload” button.

Click on the Upload button

Click the "Add files" and “Add folder” button, and upload the Student-ready starter code folder content from your local computer to the S3 bucket.

Click "Add files" to upload the index.html file, and click "Add folder" to upload the css, img, and vendor folders.


Do not select the udacity-starter-website folder. Instead, upload its content one-by-one.


Successfully uploaded starter code in the bucket

Need help with uploading the files to S3?
Sometimes the local machine's network setting or firewall might block, or the browser's Adblocker may prohibit the file upload, such as buysellads.svg file. In such a case, here are the workarounds:

Workaround 1
Try using Chrome browser, and turn off the Adblocker, if not already. Here are the steps to turn off the Adblocker in Chrome:

At the top right, click More (three dots) >> Settings.
Click Security and Privacy >> Site Settings.
Click Additional content settings >> Ads.
Turn off Block ads on sites that show intrusive or misleading ads.
Workaround 2
Use CLI commands to upload the files and folders:

Verify the AWS CLI configuration. If not configured already, use:
aws configure list
aws configure 
aws configure set aws_session_token "<TOKEN>" --profile default 
Upload files
# Create a PUBLIC bucket in the S3, and verify locally as 
aws s3api list-buckets 
# Download and unzip the udacity-starter-website.zip 
cd udacity-starter-website 
# Assuming the bucket name is my-bucket-202203081 and your PWD is the "udacity-starter-website" folder 
# Put a single file. 
aws s3api put-object --bucket my-bucket-202203081 --key index.html --body index.html 
# Copy over folders from local to S3 
aws s3 cp vendor/ s3://my-bucket-202203081/vendor/ --recursive 
aws s3 cp css/ s3://my-bucket-202203081/css/ --recursive 
aws s3 cp img/ s3://my-bucket-202203081/img/ --recursive 

