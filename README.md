# aws-elastic-beanstalk-config
This repo has the up-to-date AWS Elastic beanstalk environment config files that should be use for Devops and CI.
Dont forget to change the values in each file to match your needs


### Github workflows
The workflows are designed to follow a deploy based on the githubflow source control model.
You need to create an AWS IAM CLI Account with S3 and Elastic beanstalk access privileges and add the credentials to the github secrets (AWS_ACCESS_KEY_ID and AWS_ACCESS_SECRET).

- When there is a merge/push on the master branch, the workflow will deploy to the dev environment
- When there is a release published, the workflow will deploy to the production environment
- The CheckSource.yml workflow is used to perform compilation and tests when a pull request is created.