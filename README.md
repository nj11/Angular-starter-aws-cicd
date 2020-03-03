# Angular-starter-aws-cicd
Demonstrates creation of  a CI CD pipeline in AWS for a Angular boot application.The sample Angular Boot application used for this exercise resides at this location
```https://github.com/nj11/Angular_starter```
The AWS CI / CD tools used  are AWS Code Build,AWS Code Pipeline and AWS Beanstalk for deployment environment.


# Pre-requisites
Amazon developer console account login.If you don't have an account create it here.
```https://aws.amazon.com/console/```


#Environment

* GitHub --> Code Repository
* AWS Beanstalk --> Deployment environment
* AWS CodeBuild --> Build tool that builds artifacts from source code
* S3 --> Artifacts are staged here after build.
* AWS CodePipeline --> Code checked into Github triggers a AWS build which deploys artifacts to S3 and then deploys them to AWS Beanstalk environment.


![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/highleveldiagram.png)
