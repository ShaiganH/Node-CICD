This is a Node.js web app I made to show the benefits of cloud computing ☁️.
I also added a full DevOps pipeline using:

1. Docker
2. GitHub Actions
3. AWS EC2
4. Nginx

Every time I push code to the main branch, the app is automatically containerized and deployed to my EC2 server using Nginx 

GitHub Actions Workflow
I created a .github/workflows/deploy.yml file to set up the CI/CD pipeline.

It does this:

On every push to main, it builds the Docker image.

Then it connects to the EC2 server using SSH.

Pulls the latest code.

Builds the Docker container on EC2.

Runs the app using Nginx.

I stored my EC2 private key, host, and username in GitHub Secrets.
