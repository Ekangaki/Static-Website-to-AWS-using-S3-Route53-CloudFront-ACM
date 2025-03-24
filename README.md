# Static-Website-to-AWS-using-S3-Route53-CloudFront-ACM
Deploying a Static Website to AWS using S3, Route53, CloudFront and ACM



# S3-bucket-policy

This bucket policy allows anyone (the wildcard "*" in the "Principal" field) to read (Get) objects from the specified Amazon S3 bucket ("Bucket-Name") and its subdirectories, making the objects publicly accessible for viewing or downloading.

{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": [
                "s3:GetObject"
            ],
            "Resource": [
                "arn:aws:s3:::Bucket-Name/*"
            ]
        }
    ]
}
