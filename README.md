[![CircleCI](https://dl.circleci.com/status-badge/img/gh/NewthingAde/Continuous-Integration-Deployment/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/NewthingAde/Continuous-Integration-Deployment/tree/main)


# Introduction

Using AWS Cloud-Formation, Ansible and Circle CI tools to design and build complete CI/CD pipelines 

- ### What Is Continuous Integration, Delivery and Deployment?

Every employee must take responsibility for continuous improvements to products, services, and processes for an organisation to be effective. Improvements can reduce errors or waste, add value or safety, or address issues that slow down or irritate users.

Companies will occasionally engage in significant improvement projects, but a continuous improvement mindset means that a professional is always looking for and acting on even the smallest opportunities for improvement. Even when things are going well, a professional always looks for ways to improve.
- ### Continuous Integration

![1_YJjbmjj9UkDv1gleLsEtZw](https://user-images.githubusercontent.com/80678596/176104462-2f6b5c58-7894-43d6-9bd3-7d560d686a55.png)

Continuous integration allows development teams to quickly integrate code changes into a shared storage space. Along with automated versioning and pre-integration testing, this capability ensures that only fully functional application code is available for distribution.
- ### Continuous Deployment

![cicdcd](https://user-images.githubusercontent.com/80678596/176104640-2c720cf2-efb0-4d00-92a1-6597c92a301d.png)

Continuous deployment is a software release strategy in which any code commit that passes the automated testing phase is automatically released into the production environment, resulting in visible changes to the software's users.


- ### Continuous Delivery

![what-is-continuous-delivery](https://user-images.githubusercontent.com/80678596/176105234-72a2947d-ae4d-42d1-942c-6ab88900ba89.jpeg)

Continuous delivery is a software development practice in which code changes are automatically prepared for production release. Continuous delivery, a pillar of modern application development, extends on continuous integration by deploying all code changes to the testing and/or production environment following the build stage.
## Why CI/CD?

CI/CD enables organizations to ship software quickly and efficiently. CI/CD enables an efficient process for bringing products to market faster than ever before, continuously delivering code into production, and ensuring an ongoing flow of new features and bug fixes via the most efficient delivery method.

![0_KB2oUiVeUuC_zlAc](https://user-images.githubusercontent.com/80678596/176105486-0cf75398-337b-420a-b6d9-321c1b476594.png)

- ### The benefit of CI/CD?

 - Smaller Code Changes
 - Fault Isolations
 - More Test Reliability
 - Increase Team Transparency and Accountability
 - Faster Release Rate
 - Customer Satisfaction
 - Smaller Backlog
 - Reduced Cost
 - Easy Maintenance and Updates


### Dependencies

* Git SCM
* SSH client like OpenSSH
* NodeJs v10 or higher (if you plan on compiling locally)

## Getting Started 

- Create AWS Account
- Create IAM user for programmatic access only and copy the access key id and secret access key
- Create a PostgreSQL database in RDS that has public accessibility.
- Create a public S3 bucket with a unique name
- Build our frontend and banckend
- Test frontend and Backend
- Analysis frontend and backend
- Add SSH Key pair from EC2 to the CircleCI 
- Add environment variables to our circle ci

            AWS_ACCESS_KEY_ID=(from IAM user with programmatic access)
            AWS_SECRET_ACCESS_KEY= (from IAM user with programmatic access)
            AWS_DEFAULT_REGION=(your default region in aws)
            TYPEORM_CONNECTION=postgres
            TYPEORM_MIGRATIONS_DIR=./src/migrations
            TYPEORM_ENTITIES=./src/modules/domain/**/*.entity.ts
            TYPEORM_MIGRATIONS=./src/migrations/*.ts
            TYPEORM_HOST={your postgres database hostname in RDS}
            TYPEORM_PORT=5432 (or the port from RDS if it’s different)
            TYPEORM_USERNAME={your postgres database username in RDS}
            TYPEORM_PASSWORD={your postgres database password in RDS}
            TYPEORM_DATABASE=postgres {or your postgres database name in RDS}

- Create our infrastructure 
- Configure our Infrastructure 
- Create a database Migration
- Deploy frontend
- Deploy backend