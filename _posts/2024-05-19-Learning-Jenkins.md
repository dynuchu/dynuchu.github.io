---
title: "Learning Jenkins"
date: 2024-05-19 00:00:00 +0000
categories: [DevOps, Jenkins]
tags: [DevOps, Jenkins]
---

# Where Are We?

Hello again! I’m excited to share my progress on my journey to becoming a DevOps Engineer. So far, I’ve covered a lot of ground, from Linux basics to the essentials of cloud computing. Now, it’s time to dive into one of the key tools in the DevOps toolkit: Jenkins.

## What I've Covered So Far

### Linux Basics
Understanding the foundations of Linux is crucial for any DevOps professional. I've learned how to navigate the filesystem, manage users and permissions, and utilize essential command-line tools. These skills are the building blocks for more advanced topics.

### Virtualization
Virtualization allows for the creation of multiple virtual machines (VMs) on a single physical machine, making resource management more efficient. I’ve explored different virtualization technologies and automated the process of creating VMs using tools like Vagrant.

### Bash Scripting
Automation is a cornerstone of DevOps, and bash scripting is a powerful tool for automating repetitive tasks. I've written scripts to streamline processes, making my workflow more efficient and error-free.

### Cloud Computing
I’ve also delved into the basics of AWS and Azure. These platforms offer a wide range of services that are essential for modern infrastructure management. Understanding how to leverage these services is key to managing scalable and resilient systems.

## Getting Started with Jenkins

Now, I’m turning my attention to Jenkins, a popular open-source automation server. Jenkins is widely used for continuous integration and continuous delivery (CI/CD), which are critical practices in DevOps.

### What is Jenkins?

Jenkins automates the building, testing, and deployment of applications, making it easier to integrate changes continuously. It supports various version control tools, including Git, and can be extended with a wide range of plugins to fit different project needs.

### Setting Up Jenkins

Here’s a step-by-step guide on how to set up Jenkins on your local machine:

1. **Install Java**: Jenkins requires Java to run. Ensure you have the latest version of Java installed.
   ```bash
   sudo apt update
   sudo apt install openjdk-11-jdk
   ```

2. Add Jenkins Repository: Add the Jenkins Debian repository to your system.
    ```bash
    wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
    sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
    ```

3. Install Jenkins: Update your package index and install Jenkins.
    ```bash
    sudo apt update
    sudo apt install jenkins
    ```

4. Start Jenkins: Start the Jenkins service.
    ```bash
    sudo systemctl start jenkins
    sudo systemctl enable jenkins
    ```

5. Access Jenkins: Open your web browser and navigate to http://localhost:8080. You’ll see the Jenkins setup screen. Follow the on-screen instructions to complete the setup.

### Initial Configuration
Once Jenkins is up and running, you’ll need to unlock it with the initial admin password. This password can be found in the following file:
    ```bash
    sudo cat /var/lib/jenkins/secrets/initialAdminPassword
    ```

Copy the password and paste it into the setup screen to unlock Jenkins. From there, you can install recommended plugins and create your first admin user.

### Creating Your First Job
After the initial setup, you can create your first Jenkins job:

1. New Item: Click on “New Item” in the Jenkins dashboard.
2. Enter Job Name: Provide a name for your job.
3. Select Job Type: Choose “Freestyle project” and click “OK”.
4. Configure Job: Configure your job by setting up the source code repository, build triggers, and build steps.
5. Save and Build: Save the configuration and click “Build Now” to run your job.

### Conclusion

Getting started with Jenkins marks a significant milestone in my DevOps journey. With Jenkins, I can automate the build, test, and deployment processes, which are crucial for maintaining a robust and efficient workflow. Stay tuned as I continue to explore more DevOps tools and practices!