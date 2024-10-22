Read Me (CI/CD)

- Created S3 bucket "project-frontend-pipeline" and "backend-node-pipeline"
- Created Code pipleline for frontend and backend
- Run Clouldfromation mainpipeline.yml
- Deploy API gateway
- Update API url from code.
- Update bucket policy of "project-frontend-pipeline" S3 bucket.

{
"Version": "2012-10-17",
"Statement": [
{
"Effect": "Allow",
"Principal": {
"CanonicalUser": "<CLOUDFRONT_CANONICAL_USER_ID>"
},
"Action": "s3:GetObject",
"Resource": "arn:aws:s3:::project-frontend-pipeline/*"
}
]
}
