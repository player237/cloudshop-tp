# Phase B2 — Week 4 (multi-cloud)

## Table

| Need | AWS | Azure | GCP |
|------|-----|-------|-----|
| VM | EC2 |Virtual Machines |Computer |
| Object storage | S3 | | Cloud storage|
| DNS | Route 53 |Azure DNS |Cloud DNS |
| CI | CodeBuild |Azure DevOps |Cloud Build |

## Question

Why use **GitHub Actions** instead of installing Jenkins on your own VM? (5 lines)

•No server to maintain: Jenkins requires you to install, update, and secure a server yourself. GitHub Actions is fully managed, GitHub does all of that for you.

•Zero setup cost: GitHub Actions is free for public repos and also free for private ones. Jenkins on EC2 costs money 24/7.

•Integrated with your code: GitHub Actions runs directly in the same platform where your code lives, with no extra configuration to connect to your repository.

•Instant scalability: GitHub automatically provides fresh virtual machines (runners) for each pipeline run. With Jenkins, you need to add more machines manually to run parallel jobs.

•Security: GitHub Actions handles secrets management, TLS, and runner isolation. With Jenkins on your own VM, you are responsible for all of this yourself.
