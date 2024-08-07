+++
title = 'Building This Site'
date = 2024-08-07T12:45:01-04:00
draft = false
layout = "simple"
+++

Back in the early 2000s, I created gaming-related sites and blogs using PHP and Wordpress. Now, I thought it would be a nice idea to dive back a bit into the web with a personal website. It's also a good excuse to explore AWS services.

This site is built using [Hugo](https://gohugo.io/) and the [Congo theme](https://themes.gohugo.io/themes/congo/). It is deployed to AWS via a Github action.
Here's a quick rundown of what I did:
- Purchased a domain name
- Requested an SSL Certificate through AWS Certificate Manager
- Created an S3 bucket to store my site
- Setup CloudFront distribution with the S3 bucket as the Origin
- Added the Custom SSL Certificate and the domain name to my CloudFront distribution once the certificate was ready
- Pushed my Hugo Site to Github
- Created a [Github action](https://github.com/rkhalife/rkhalife.ca/blob/main/.github/workflows/main.yml) to automatically update the S3 bucket whenever I push changes
