# web-app-k8s
This project aims for the implementation of CICD and GitOps for web applications using a range of DevOps tools including Git, Jenkins, SonarQube, Maven, Docker, Kubernetes and  Argo CD.

Prerequisites:
General knowledge of server/instance creation on any cloud i.e., AWS, GCP, Azure, Oracle.
Basics of Jenkins pipeline syntax.
Basic understanding of various DevOps tools like SonarQube, Maven, Docker, Kubernetes and Argo CD.
Tools used:
Jenkins
SonarQube
Maven
Docker
Kubernetes
Argo CD
Project Brief:
This project aims to guide the process of automatic deployment of a web application on the Kubernetes cluster over the Apache Tomcat web server.

You can use any of the code as you can get many on the internet or use the same code that I used through the GitHub repo.
Initially, developer will commit the code to GitHub repository, GitHub will trigger the code changes to Jenkins pipeline.
Jenkins pipeline will be configured with the SonarQube which will Continuously Inspect the code for bugs, code smells, and security vulnerabilities through defined quality gates.
Code will be packaged through code build using maven, later will copy the .war or .jar or .ear file i.e., maven build file into tomcat image, to achieve custom built image, this will be pushed to the docker hub repository.
Kubernetes manifest file will be automatically updated with the latest docker image tag and will be pushed to configuration repository of GitHub.
Argo CD a GitOps tool, will pull the changes and sync the application to desired state whenever the changes are made to the configuration repository.
Once the CICD pipeline is finished, the complete process will be automated so that you can deploy the updated code with just one click by utilizing different deployment strategies of Kubernetes. Then the Argo CD will sync the application for desired state.
