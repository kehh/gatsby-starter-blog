---
title: Experimenting with Amplify as a CI/CD framework for managing this site.
date: "2019-07-18"
---

I'm running this site using the static site generator, [Gatsby.js](https://www.gatsbyjs.org/). I've been interested in 
AWS Lambda and Serverless for some time. However I've also not been sure how to best use it for hosting a blog. 
Then along came [AWS Amplify Console](https://aws.amazon.com/amplify/console/) which has made it possible to host a gatsby page with CI/CD 
for the content.

All I have to do is create a Markdown page, commit it and push it and a new version of the site gets deployed into
an S3 bucket. The AWS console will email me on builds & failures.

Additionally I can have as many environments as I like just by configuring a branch in the console.

