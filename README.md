# web-app-k8s
This project aims for the implementation of CICD and GitOps for web applications using a range of DevOps tools including Git, Jenkins, SonarQube, Maven, Docker, Kubernetes and  Argo CD.

## Prerequisites:
1. General knowledge of server/instance creation on any cloud i.e., AWS, GCP, Azure, Oracle.
2. Basics of Jenkins pipeline syntax.
3. Basic understanding of various DevOps tools like SonarQube, Maven, Docker, Kubernetes and Argo CD.

## Tools used:
1. Jenkins
2. SonarQube
3. Maven
4. Docker
5. Kubernetes
6. Argo CD

## Project Brief:
> This project aims to guide the process of automatic deployment of a web application on the Kubernetes cluster over the Apache Tomcat web server.

![Alt text](https://47627754-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FQ2eA6wdhFG1vJALtBXmC%2Fuploads%2FrN5j1WL1Nvw4FVuPq3NE%2Fimage.png?alt=media&token=5720c50c-a2fa-4ff4-9a2f-a05c34fd01f6)

1. You can use any of the code as you can get many on the internet or use the same code that I used through the GitHub repo.
2. Initially, developer will commit the code to GitHub repository, GitHub will trigger the code changes to Jenkins pipeline.
3. Jenkins pipeline will be configured with the SonarQube which will Continuously Inspect the code for bugs, code smells, and security vulnerabilities through defined quality gates.
4. Code will be packaged through code build using maven, later will copy the .war or .jar or .ear file i.e., maven build file into tomcat image, to achieve custom built image, this will be pushed to the docker hub repository.
5. Kubernetes manifest file will be automatically updated with the latest docker image tag and will be pushed to configuration repository of GitHub.
6. Argo CD a GitOps tool, will pull the changes and sync the application to desired state whenever the changes are made to the configuration repository.
7. Once the CICD pipeline is finished, the complete process will be automated so that you can deploy the updated code with just one click by utilizing different deployment strategies of Kubernetes. Then the Argo CD will sync the application for desired state.
