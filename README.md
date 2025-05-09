# MYWEBSITE 
CI/CD Pipeline for Static Website

This project sets up a simple CI/CD pipeline for a static HTML website using GitHub, Python, Bash scripts, Cron jobs, and Nginx on an Ubuntu server.

Technology Used:
- Git and GitHub for version control
- Python script to check for new commits on GitHub
- Bash script to deploy code to the web server
- Cron job to run scripts every 5 minutes
- Nginx web server to serve the website

Files Included:
- index.html: Your static website content
- check_github.py: Checks for new commits on the GitHub repository
- update_website.sh: Pulls the latest code and syncs it with the Nginx web root
- ci_cd_wrapper.sh: Runs the Python check and deploys if updates are found

How it works:
1. You push changes to your GitHub repository.
2. The server runs a cron job every 5 minutes.
3. The cron job calls a wrapper script.
4. The Python script checks GitHub for new commits.
5. If changes are found, the Bash script deploys the latest code.
6. The website is automatically updated and served via Nginx.

Cron Job Example:
*/5 * * * * /home/ubuntu/ci_cd_wrapper.sh >> /home/ubuntu/ci_cd.log 2>&1

![image](https://github.com/user-attachments/assets/a19d987c-5519-4eeb-bfbb-d382d65b91d9)
