# flask-aws-ec2-nginx-deployment
Deployed a Flask web application on AWS EC2 using Gunicorn and Nginx with hands-on troubleshooting and cloud networking.
# Flask AWS EC2 Deployment with Nginx and Gunicorn

**Description:**  
This project demonstrates deploying a Python Flask web application on an AWS EC2 instance using Gunicorn as the application server and Nginx as a reverse proxy. The focus of this project was hands-on learning, troubleshooting, and understanding cloud deployment workflows.

---

## Project Overview

The application is a simple Flask web app that returns a message to users. While the app itself is lightweight (~10 lines of code), the project showcases real-world cloud deployment experience including server setup, networking, and troubleshooting.

Key highlights:

- Deployed a Flask application on AWS EC2  
- Configured Gunicorn for application serving  
- Set up Nginx as a reverse proxy  
- Managed AWS security groups to allow HTTP and SSH access  
- Practiced troubleshooting real-world deployment issues

---

## Tech Stack

- **Cloud Provider:** AWS EC2 (Amazon Linux)  
- **Backend:** Python (Flask)  
- **Application Server:** Gunicorn  
- **Web Server / Reverse Proxy:** Nginx  
- **Tools:** Linux CLI, SSH, Security Groups

---

## Architecture

The user accesses the app through Nginx, which forwards requests to Gunicorn running the Flask application.

---

## Setup / Deployment Steps (High-Level)

1. Launch an AWS EC2 instance (Amazon Linux)  
2. Configure security groups for SSH (port 22) and HTTP (port 80) access  
3. Install Python, Flask, Gunicorn, and Nginx on the instance  
4. Create a simple Flask app (`app.py`)  
5. Run the Flask app with Gunicorn  
6. Configure Nginx to serve as a reverse proxy to Gunicorn  
7. Test application via the public IP  

---

## Challenges & Lessons Learned

During deployment, I encountered and resolved several issues:

- SSH key recognition problems when connecting to EC2  
- Flask app not accessible due to port or security group misconfigurations  
- Port conflicts when running Gunicorn  
- Nginx configuration errors  

This taught me the importance of careful networking setup, service management, and troubleshooting skills in a cloud environment.

---

## Breaking the Application (Learning Exercise)

To simulate real-world scenarios and improve troubleshooting skills, I intentionally:

- Stopped Gunicorn → caused server errors  
- Misconfigured Nginx → disrupted routing  
- Introduced code errors → caused Flask app failures  

These exercises reinforced my understanding of **debugging and maintaining cloud applications**.

---

## Future Improvements

Next steps I plan to implement:

- Integrate a CI/CD pipeline using GitHub Actions  
- Use Terraform or CloudFormation for automated provisioning  
- Containerize the Flask application with Docker  

---

## Key Takeaways

- Deploying a web app in the cloud requires attention to networking, security, and server configuration  
- Troubleshooting real-world deployment issues is a valuable learning experience  
- Documenting the process makes it easier to showcase skills to recruiters and hiring managers

---

## Demo

Once deployed, accessing the public IP of the EC2 instance displays:
