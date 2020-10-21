# NoteJam-migration-on-ElasticBeanstalk

# Notejam application stack
Provision: CloudFormation
CI/CD: CodePipeline/CloudBuild with CodeCommit integration
App: Elastic Beanstalk
Database: RDS (mysql)
Monitoring: Cloudwatch
Logs: Cloudwatch for app logs as well as S3.
Lambda functions is being used to get and generate passwords for RDS master account.

# Prereqs:
Create an S3 bucket and place the lambda functions "generate-password-lambda.zip" and "get-password-lambda.zip"located in presentation/lambdafunctions folder, please note that the format should be .zip.
In the AWS account which the stack will be executed, create an repository in CodeCommit and push all the files in this repository except the presentation folder.

# Execution:
Execute the notejam-cf-stack.yml template from CloudFormation located in presentation/cloudformation folder. Please note that you also need to specify all parameters when deploying such as lambda functions bucketname etc.

Information, improvements and architecture can be found in the presentation folder in this repo.
