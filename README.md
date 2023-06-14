# Jenkins CI/CD Jobs - Pipelines for Continuous Integration and Delivery for Powertrckr site
<a name="readme-top"></a>
<!-- ABOUT THE PROJECT -->
## About The Project

This project is Jenkins pipelines created for CI/CD process for Powertrckr site. 

CI process downloads changes to the code from the website repository, performs static code analysis in Sonarqube, then builds and saves the containers in AWS ECR and deploys them in the AWS ECS test environment. 

When all tests pass, the CD process is started, which uses the updated image and replaces it with AWS EKS, which ensures continuous delivery. This project also contains pipeline for automatic creation of AWS EKS service and setting the base page container image and DNS names in Route 53.

<!-- FUNCTIONS -->
## Functions

* Continuous Integration (CI): The CI process is triggered whenever changes are made to the codebase of the Powertrckr site. It automatically downloads the code changes from the website repository and performs static code analysis to ensure code quality.
* Containerization and Image Management: The CI process builds and saves the Docker containers in AWS ECR (Elastic Container Registry), providing a centralized location to store and manage container images for the application.
* Deployment to AWS ECS: After the containers are built, the CI process deploys them in the AWS ECS (Elastic Container Service) test environment. This allows for quick and efficient deployment of the application in a controlled and isolated environment for testing purposes.
* Automated Testing: The CI process runs automated tests on the deployed application to ensure its functionality and identify any potential issues or regressions.
* Continuous Delivery (CD): Once the tests pass successfully in the test environment, the CD process is triggered. It takes the updated container image and replaces the existing one in the AWS EKS (Elastic Kubernetes Service) production environment, enabling continuous delivery of new features and updates.
* Infrastructure Automation: The project includes a pipeline for the automated creation of the AWS EKS service. It handles the provisioning and configuration of the necessary infrastructure resources, such as networking, security, and scaling, to support the deployment and operation of the application.
* DNS Configuration with Route 53: The pipeline also handles the setting of DNS names in Route 53, the AWS service for domain name system (DNS) management. It ensures that the Powertrckr site is accessible using the desired domain names.

<!-- TECHNOLOGIES -->
## Technologies

Technologies used to create this site:
* ![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)
* ![Groovy](https://img.shields.io/badge/Groovy-4298B8?style=for-the-badge&logo=apache%20groovy&logoColor=white)
* ![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?style=for-the-badge&logo=sonarqube&logoColor=white)
* ![AWS ECS](https://img.shields.io/badge/AWS%20ECS-232F3E?style=for-the-badge&logo=amazon%20aws&logoColor=white)
* ![AWS EKS](https://img.shields.io/badge/AWS%20EKS-232F3E?style=for-the-badge&logo=amazon%20aws&logoColor=white)
* ![Route 53](https://img.shields.io/badge/Route%2053-232F3E?style=for-the-badge&logo=amazon%20route%2053&logoColor=white)

<!-- INSTALLATION -->
## Installation

To install and configure this project, follow these steps:
* Jenkins: Install Jenkins on your server or in the cloud. Configure it according to your requirements and access to the code repository.
* Install required Jenkins plugins:

  SonarQube Scanner Version 2.15

  Build Timestamp Version 1.0.3

  Pipeline Maven Integration Version 1279.v5d711113020f

  Pipeline Utility Steps Version 2.15.1

  Docker Pipeline Version 563.vd5d2e5c4007f

  Amazon ECR Version 1.114.vfd22430621f5

  Amazon Web Services SDK :: All Version 1.12.406-374.v4cdf53953691

  CloudBees Docker Build and Publish Version 1.4.0

* Setup required secrets for AWS and kubectl. 
* Create pipelines in Jenkins from Jenkinsfiles
  
<!-- AUTHOR -->
## Author

Email: kudlatyicss@gmail.com

GitHub: [https://github.com/fanfanafankianki]

Website Project link: [https://github.com/fanfanafankianki/gym_progress_site]

Tests for site Project link: [https://github.com/fanfanafankianki/Tests_Gym_Progress_Site]

Jenkins CI/CD Project link: [https://github.com/fanfanafankianki/Jenkins_CICD_Website]
<p align="right">(<a href="#readme-top">back to top</a>)</p>
