# automated-interview-organization
Implementation of an automated interview organization system as part of my final project for Info 202 at the Berkeley I-School. Leverages AWS.  

### Part 0 - Setting up AWS & Uploading initial interview files
Too use this tool some prior setup of AWS is required.

It is highly recommended to install and configure the AWS CLI on your local machine. A good article giving steps to do this can be found here:
https://medium.com/@mehmetodabashi/how-to-install-and-configure-aws-cli-on-windows-10-3c8decffc507

After setting up your AWS to use this tool it is also require to create 4 buckets:
    1. A bucket for your interview audio files
    2. A bucket for your interview transcript files
    3. A bucket for your model output
    4. (Optional) A bucket for your custom classifier data 
Documentation on how to create buckets can be found here: https://docs.aws.amazon.com/AmazonS3/latest/userguide/create-bucket-overview.html

Finally, before getting started, upload ALL interview files to your created bucket designated for interview audio files.
Documentation on how to upload to a bucket can be found here: https://docs.aws.amazon.com/AmazonS3/latest/userguide/upload-objects.html


### Creating your custom classifier
This tool is best suited for use alongside a custom classifier trained to your style of interviews.
What this will look like on the users end is a CSV with classes alongside documents fitting those classes.
An example can be found in the repo called: "example_classifier_data.csv"
Additionally documentation for this can be found here: https://docs.aws.amazon.com/comprehend/latest/dg/how-document-classification.html


Resources used in this project:
Amazon S3 - https://us-east-2.console.aws.amazon.com/s3/get-started?region=us-east-1&bucketType=general
Amazon Transcribe - https://us-east-1.console.aws.amazon.com/transcribe/home?region=us-east-1#welcome
Amazon Comprehend - https://us-east-1.console.aws.amazon.com/comprehend/home?region=us-east-1#welcome
AWS Boto3 - https://aws.amazon.com/sdk-for-python/
tscribe - https://pypi.org/project/tscribe/
