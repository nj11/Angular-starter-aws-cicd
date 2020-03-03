# Angular-starter-aws-cicd
Demonstrates creation of  a CI CD pipeline in AWS for a Angular boot application.

The sample Angular Boot application used for this exercise resides at this location
```https://github.com/nj11/Angular_starter```

The AWS CI / CD tools used  are:
 * AWS CodeBuild
 * AWS CodePipeline 
 * AWS Beanstalk for deployment environment.


# Pre-requisites
Amazon developer console account login.If you don't have an account create it here.
```https://aws.amazon.com/console/```


# Environment

* GitHub --> Code Repository
* AWS Beanstalk --> Deployment environment
* AWS CodeBuild --> Build tool that builds artifacts from source code
* S3 --> Artifacts are staged here after build.
* AWS CodePipeline --> Code checked into Github triggers a AWS build which deploys artifacts to S3 and then deploys them to AWS Beanstalk environment.


![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/highleveldiagram.png)

# Step 1 : Beanstalk environment creation.

* Sign in to to AWS console using your account .Navigate to ```My Account--> AWS Management Console.```
Go to  ```Services-->Elastic beanstalk```   and then select ```Create a new application.```
       
![Alt desc](https://github.com/nj11/Angular_starter/blob/master/screenshots/aws1.png)


![Alt desc](https://github.com/nj11/Angular_starter/blob/master/screenshots/aws2.png)

* Select the appropriate tier.In this case we are selecting Web server environment.

* Enter your application details.

![Alt desc](https://github.com/nj11/Angular_starter/blob/master/screenshots/aws3.png)

* Enter application platform, in this case it's Java

![Alt desc](https://github.com/nj11/Angular_starter/blob/master/screenshots/aws4.png)

* For now choose sample application.We will upload and deploy application jar later.
![Alt desc](https://github.com/nj11/Angular_starter/blob/master/screenshots/aws5.png)

* Environment creation takes a few minutes.

![Alt desc](https://github.com/nj11/Angular_starter/blob/master/screenshots/aws6.png)

* Once the environment is ready, click on the enviornment name link as highlighted.

![Alt desc](https://github.com/nj11/Angular_starter/blob/master/screenshots/aws7.png)

* You can check the environment page, along with configuration details like enviornment variables,logs and application URL.

![Alt desc](https://github.com/nj11/Angular_starter/blob/master/screenshots/aws8.png)

# Step 2 : AWS Pipeline creation including creating the build stage

* Make sure the buildspec.yml exists in the root folder of your github project


![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/buildspec.png)


![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/pipeline1.png)

![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/pipeline2.png)

![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/pipeline3.png)


![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/pipeline4.png)

![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/pipeline5.png)

![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/pipeline6.png)

![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/pipeline7.png)

![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/pipeline8.png)

![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/pipeline9.png)

![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/pipeline10.png)

![Alt desc](https://github.com/nj11/Angular-starter-aws-cicd/blob/master/screenshots/pipeline11.png)

