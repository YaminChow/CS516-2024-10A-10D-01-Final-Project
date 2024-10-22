Read Me (CI/CD)

- Created S3 bucket "project-frontend-pipeline" and "backend-node-pipeline"
- Created Code pipleline for frontend and backend
- Run Clouldfromation mainpipeline.yml
- Deploy API gateway
- Update API url from code.
- Update bucket policy of "project-frontend-pipeline" S3 bucket.
- Create invalidation of CloudFront

{
"Version": "2008-10-17",
"Id": "PolicyForCloudFrontPrivateContent",
"Statement": [
{
"Sid": "AllowCloudFrontServicePrincipal",
"Effect": "Allow",
"Principal": "*",
"Action": "s3:GetObject",
"Resource": "arn:aws:s3:::project-frontend-pipeline/*",
"Condition": {
"StringEquals": {
"AWS:SourceArn": "arn:aws:cloudfront::361769602049:distribution/E2TCMQT2K9LKHG"
}
}
}
]
}

Frontend: https://github.com/YaminChow/Final-project-cloud-frontend
Backend: https://github.com/YaminChow/Final-Project-Cloud-Backend
Document: https://github.com/YaminChow/CS516-2024-10A-10D-01-Final-Project
