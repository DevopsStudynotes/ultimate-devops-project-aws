# Runnning the entire project as containers in a single VM - Steps involved:

    1. Create an IAM user for project.
    2. Setup keys for the user.
    3. Create an EC2 instance with t2.large and ubuntu image. Keys can be created while ec2 is being created.
    4. Install docker for ubuntu. Lookup installation information in Docker docs website. Alternatively, use docker desktop and install it in your computer. Link for Ubuntu installation: https://docs.docker.com/engine/install/ubuntu/
    5. Use the below command (to add ubunutu user to docker group) if you do not want to use sudo for every command. 
        ```bash
        sudo usermod -aG docker ubuntu
        ```
    6. Install kubectl in your local computer (using chocolatey in windows) or ubuntu. kubectl is the client that will interact with your k8s cloud. Alternatively, you can install it in the ec2 machine that was created.
    7. Install terraform in your local machine or ec2.
    