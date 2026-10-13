# DevOps CI/CD Website Deployment

## Project Overview
This project demonstrates an automated CI/CD pipeline that deploys a static website to Amazon S3 and uses Amazon CloudFront for content delivery.

## Technologies Used
- **GitHub:** Source code management
- **GitHub Actions:** CI/CD automation
- **AWS IAM:** Authentication and permissions
- **Amazon S3:** Website file storage
- **Amazon CloudFront:** Content delivery and caching

## Architecture
Developer pushes code to the `main` branch → GitHub Actions workflow runs → AWS credentials are configured securely using GitHub Secrets → Website files are synchronized to S3 → CloudFront cache is invalidated.

## Website
**Live URL:** https://dnoqx6wfwe1mn.cloudfront.net

## Deployment Workflow
The GitHub Actions workflow:
1. Checks out the repository.
2. Configures AWS credentials using GitHub Secrets.
3. Synchronizes website files to the S3 bucket.
4. Invalidates the CloudFront cache so updated content can be served.

## GitHub Secrets
The workflow uses these repository secrets:
- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `S3_BUCKET_NAME`
- `CLOUDFRONT_DISTRIBUTION_ID`

AWS credentials are stored as GitHub Secrets rather than hardcoded in the workflow.

## Deployment Trigger
The workflow runs automatically when code is pushed to the `main` branch.

## Result
The website is successfully deployed using an automated GitHub Actions pipeline, Amazon S3, and Amazon CloudFront.
