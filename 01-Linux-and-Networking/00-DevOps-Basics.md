# Introduction to DevOps & CI/CD

## What is DevOps?
*  DevOps is the combination of Development (Dev) and Operations (Ops) teams.
* It acts as a strong pillar or bridge to fill the communication and operational gap between these teams, ensuring seamless integration and collaboration.
* The core goal is the automation of every process across both teams to continuously integrate and deliver a good product.

## The DevOps Lifecycle
The standard software delivery cycle includes the following stages: 
Code Build ➔ Code Test ➔ Code Analysis ➔ Deploy to DB/Server ➔ User Approval ➔ Go Live in Production.

## Continuous Integration & Continuous Delivery (CI/CD)

### Continuous Integration (CI)
* CI is the continuous process of building, testing, and creating software artifacts (like .war, .jar, or .zip files) with no errors.
* **Key Tools Used:**
  * **Version Control:** Git.
  * **Build, Test, and Evaluate:** Jenkins.
  * **Artifact Generation:** Maven (depending on the programming language).

### Continuous Delivery (CD)
* CD solves the problem of requiring excessive manpower for manual testing after every deployment. 
* It involves automating the testing scripts and combining them with the developer's source code.
* CD is the final stitching of every automation script into a single process, which automatically triggers the testing and deployment of the application.