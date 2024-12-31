# DeployMate: A Vercel Clone

## Setup Guide

This project contains the following services and folders:

1. **api-server**: HTTP API Server for REST APIs
2. **build-server**: Docker Image code that clones, builds, and pushes the build to S3
3. **s3-reverse-proxy**: Reverse Proxy to route subdomains and domains to S3 bucket static assets

---

## Local Setup

1. Run `npm install` in all three services:
   - `api-server`
   - `build-server`
   - `s3-reverse-proxy`

2. Docker build the `build-server` and push the image to AWS ECR.

3. Configure the `api-server` by providing all the required configs such as TASK ARN and CLUSTER ARN.

4. Start the services:
   - Run `node index.js` in `api-server` and `s3-reverse-proxy`

At this point, the following services will be up and running:

| S.No | Service           | Port |
|------|-------------------|------|
| 1    | api-server        | 9000 |
| 2    | socket.io-server  | 9002 |
| 3    | s3-reverse-proxy  | 8000 |

---

## Demo
https://drive.google.com/file/d/1lq0Js3HBUi0iSZafGm89ykZOSg5zfGmt/view?usp=sharing

---

