

# AWS Code Pipeline 

## Introduction

✍️ AWS CodePipeline is a fully managed continuous delivery service that helps you automate your release pipelines for fast and reliable application and infrastructure updates. CodePipeline automates the build, test, and deploy phases of your release process every time there is a code change, based on the release model you define. This enables you to rapidly and reliably deliver features and updates. You can easily integrate AWS CodePipeline with third-party services such as GitHub or with your own custom plugin. With AWS CodePipeline, you only pay for what you use. There are no upfront fees or long-term commitments.

## Prerequisite

✍️ 
github 
way around aws consloe

## Use Case

Learn how we to use AWS Code Pipeline to move your project code from GitHub to Amazon S3 bucket where a static website is hosted. 
Let me give you an overview of what I am going to show you. I have a demo project in my localhost, if I change anything here on the localhost project and push that to remote repository in GitHub, it will be updated there. 
But using the AWS code pipeline service, I want to get any changes, automatically replicated or updates to the AWS S3 bucket hosted static website. This will help in the way that we can write code and test in the localhost environment without affecting the live code, then we want the modifications replicated to the live website that’s hosted on AWS S3 bucket, as it is pushed from localhost to GitHub repository.
Here on the xampp projets directory that is opt/lampp/htdocs, I have a project directory named testproject. In the project directory, we have two files, index.html and error.html. I am going to host this project to AWS S3 bucket as a static website. If I modify anything in this project file locally and push it to the remote repository on GitHub, changes will automatically be replicated to the live website. 

## Cloud Research

- ✍️https://aws.amazon.com/codepipeline

## Try yourself

✍️ this will help ur process of continuous changes 

### Step 1 — Summary of Step

learn about code pipeline

### Step 2 — Summary of Step

build a project/static web page

### Step 3 — Summary of Step

deploy it on aws using code pipeline

## ☁️ Cloud Outcome

✍️ https://github.com/akaszz/github-profile-finder

The GitHub Profile Finder web app powered by GitHub API which is built using HTML/CSS, Bootstrap 4 and Vanilla Javascript

It searches for user profiles as you type but reduces unnecessary API calls using setTimeout() method. So API is only called when you have stopped typing your desired keyword.
It shows the user information like number of repos, gists, followers and following.
It fetches the 5 latest added repos with stars, watchers and forks.
User's profile and repo are directly linked to GitHub, so anyone searching on this platform would easily be able to navigate to user's GitHub profiles.
It takes care of all the edge cases for the API info returned.

here is the project deployed using code pipeline

http://mygithubprofilefinder.s3-website.ap-south-1.amazonaws.com/




