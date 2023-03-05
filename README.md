# DevOps Project - Continuous Integration and Continuous Delivery of Vprofile Project

This is a DevOps project for [CI/CD](https://www.redhat.com/en/topics/devops/what-is-ci-cd) (_Continuous Integration and Continuous Delivery_) of vprofile project using Jenkins, Nexus, SonarQube, Docker, AWS Cloud and Slack. This project is a continuation of [_vprofile-project-ci-jenkins_](https://github.com/durrezahmed/vprofile-project-ci-jenkins) project.

[Link](https://github.com/durrezahmed/vprofile-project-devops) for vprofile app repository.

## Problem - Issues with Current Situation:

- In an Agile SDLC, there will be Frequent Code changes

- Manual Code Deployment is Time Consuming

- Involves Task Assignment / Ticketing / Approvals

- Dependency on Ops, Build and Release Teams

## Solution - Fix:

- Build, Test, Deploy and Test for Every Commit

- Automated Process

- Notify for Every Build Status

- Fix Code if Bugs or Errors found Instantly rather than waiting

## Benefits - CICD Pipeline:

- Short MTTR (Mean Time to Recovery)

- No Human Intervention

- Fault Isolation

- Agile

## Tools used in the Project:

- [**Jenkins**](https://www.jenkins.io/) - Continuous Integration and Continuous Delivery Server

- [**Git and GitHub**](https://github.com/) - Version Control System

- [**Maven**](https://maven.apache.org/) - Build Tool

- [**Checkstyle**](https://checkstyle.org/) - Code Analysis Tool

- [**Nexus Sonatype Repository**](https://www.sonatype.com/products/nexus-repository) - Artifact / Software Repository

- [**SonarQube**](https://www.sonarsource.com/products/sonarqube/) - Code Analysis Server

- [**Docker**](https://www.docker.com/) - Build Docker Images

- [**Amazon EC2**](https://aws.amazon.com/ec2/) - Compute Resource

- [**Amazon ECR**](https://aws.amazon.com/ecr/) - Elastic Container Registry

- [**Amazon ECS**](https://aws.amazon.com/ecs/) - Elastic Container Service

- [**AWS CLI**](https://aws.amazon.com/cli/) - AWS Command Line Interface

- [**Slack**](https://slack.com/) - Notifications

## Jenkins Plugins used in the Project:

- [**Maven Integration**](https://plugins.jenkins.io/maven-plugin/)

- [**GitHub Integration**](https://plugins.jenkins.io/github-pullrequest/)

- [**Nexus Artifact Uploader**](https://plugins.jenkins.io/nexus-artifact-uploader/)

- [**SonarQube Scanner**](https://plugins.jenkins.io/sonar/)

- [**Build Timestamp**](https://plugins.jenkins.io/build-timestamp/)

- [**Docker Pipeline**](https://plugins.jenkins.io/docker-workflow/)

- [**CloudBees Docker Build and Publish**](https://plugins.jenkins.io/docker-build-publish/)

- [**Amazon ECR**](https://plugins.jenkins.io/amazon-ecr/)

- [**Pipeline: AWS Steps**](https://plugins.jenkins.io/pipeline-aws/)

- [**Slack Notification**](https://plugins.jenkins.io/slack/)

## Usage (Flow of Execution) - Jenkins CICD Steps:

1. Update GitHub Webhook with new Jenkins IP

2. Copy Docker Files from the Repository

3. Create Two Separate Jenkinsfile for staging and production in Source Code

4. AWS Steps

   a. IAM Setup

   b. ECR Repository Setup

5. Jenkins Steps

   a. Install Plugins

   - Docker Pipeline

   - CloudBees Docker Build and Publish

   - Amazon ECR

   - Pipeline: AWS Steps

6. Install Docker Engine and AWS CLI on Jenkins Server

7. Write Jenkinsfile for Build and Publish Image to ECR

8. ECS Setup

   a. Cluster Setup

   b. Task Definition Setup

   c. Service Setup

9. Code for Deploying Docker Image to ECS

10. Repeat the Steps for Production ECS Cluster

11. Promoting Docker Image for Production
