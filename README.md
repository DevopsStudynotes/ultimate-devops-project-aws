# Notes for Ultimate DevOps Project and Resume Preparation Udemy Course

- This repository contains the complete notes for the Ultimate DevOps Project and Resume Preparation course prepared by `Abhishek Veeramalla` on Udemy.

- Documentation is organized in Sections, the same way how videos are organized in the udemy course.

## Runnning the entire project as containers in a single VM - Steps involved:

    1. Create an IAM user for project.
    2. Setup keys for the user.
    3. Create an EC2 instance with t2.large and ubuntu image. Keys can be created while ec2 is being created.
    4. Install docker for ubuntu. Lookup installation information in Docker docs website. Alternatively, use docker desktop and install it in your computer.
    5. Install kubectl in your local computer (using chocolatey in windows) or ubuntu. kubectl is the client that will interact with your k8s cloud. Alternatively, you can install it in the ec2 machine that was created.
    6. Install terraform in your local machine or ec2.
    7. If you only used 8G to create a volume during ec2 creation, this might have to be expanded for the installation of the pre-requisites for this project. Use the following commands:
        
        To check partition info and to note down name of the partition assigned to root folder:
        
        ```bash
        df -h
        lsblk
        ```
        
        To increase the size of the partition (assuming xvda1 is the root partition):
        ```bash
        sudo apt install cloud-guest-utils
        sudo growpart /dev/xvda1
        ```

        To verify partition size has been changed:
        ```bash
        lsblk
        ```

        To update the filesystem so that it reflects the size change for root directory:
        ```bash
        sudo resize2fs /dev/xvda1
        ```
    8. To run containers in the background:
        ```bash
        docker compose up -d
        ```
    9. To access the project on the browser, AWS security group rules need to be modified. Note: SG blocks everything by default, NACL allows everything by default. Edit SG of EC2 to allow SSH from anywhere and port 8080 from anywhere. Access frontend by using http://<IP-of-EC2>:8080.

## 





