# Build CI/CD Pipelines

Udacity DevOps course pipeline

This repo is created during Build CI/CD Pipelines Udacity Cloud DevOps course.

It contains:
- Jenkinsfile
- index.html

## Prerequisites

Jenkins server with following components installed & configured:
- Blueocean plugin
- Aqua Jenkins MicroScanner plugin
- Set up IAM user, role, group & policy in AWS
- CloudBees AWS Credentials Plugin

## Jenkinsfile

Contains the definition of a Jenkins Pipeline and four-stage continuous deployment pipeline.

### 1. Stage Build
The sh steps invoke echo and curl commands. The last step check if URL is accessible and returns exit code.
Any non-zero exit code will fail the Pipeline.

### 2. Stage Lint HTML
The step in this stage orrects and cleans up HTML in all html files. Any error in the code will fail the Pipeline.

### 3. Stage Security Scan
Enables scanning of docker builds in Jenkins for OS package vulnerabilities using Aqua Jenkins MicroScanner Plugin.

### 4. Stage Upload to AWS
Upload content to AWS S3 with AWS credentials.

## Resources

* [owreadjenkins](https://github.com/owreadjenkins/course3lesson2)


## License

The contents of this repository are covered under the [GNU General Public License](LICENSE).
