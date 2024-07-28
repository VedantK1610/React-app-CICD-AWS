# React App CI/CD Pipeline on AWS

## Overview
This project demonstrates a CI/CD pipeline setup for a React app using AWS services such as S3, CodeBuild, and CodePipeline. The React app is automatically built and deployed to an S3 bucket.

## Features
- Automated build and deployment using CodePipeline
- Hosting of React app on S3 with static website hosting
- Integration with GitHub for source control

## Architecture
- **Source**: GitHub repository containing the React app.
- **Build**: AWS CodeBuild project to build the app.
- **Deploy**: AWS S3 bucket to host the app.

![Screenshot_2](https://github.com/VedantK1610/React-app-CICD-AWS/blob/main/Screenshot%202024-07-28%20125313.png)

## Prerequisites
- Node.js
- AWS Account
- GitHub Account

## Steps to Set Up CI/CD
**Create an S3 Bucket**:
- Go to the S3 console and create a new bucket named my-react-app-bucket.
- Enable static website hosting and set index.html as the index document.

**Set Up CodeBuild**:
- Go to the CodeBuild console and create a new build project named ReactAppBuild.
- Configure the source provider as GitHub and connect your repository.
- Define the buildspec file in the repository for build commands.

**Set Up CodePipeline**:
- Go to the CodePipeline console and create a new pipeline named ReactAppPipeline.
- Add GitHub as the source provider and select your repository.
- Add CodeBuild as the build provider and select your build project.
- Add S3 as the deploy provider and specify your S3 bucket.

## Deployment
The app is deployed to an S3 bucket and can be accessed at http://react-cicd-project.s3-website.ap-south-1.amazonaws.com 

## Credits
This React app was originally developed by [Original Developer's Name](https://github.com/thehyperart11) . Special thanks to them for their work on this project.
