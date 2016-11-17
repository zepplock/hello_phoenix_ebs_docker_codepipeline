# HelloPhoenix On AWS Elastic Beanstalk, Docker, CodePipeline

## AWS Elastic Beanstalk installation guide

Create a new EBS application called `hello_phoenix`

Create a new environment using Docker platform. Choose a `Sample application` for now.

Update configuration to have `ENV` `prod` under `Software Configuration`

## AWS CodePipeline configuration

Step 1: Go to AWS CodePipeline and create a new pipeline, name it `hello_phoenix`

Step 2a: Select `GitHub` as a source provider

Step 2b: Click on `Connect to GitHub` button

Step 2c: After being redirected to GitHub, enter your username and password

Step 2d: Enter repository name and branch

Step 3: Choose `No Build`

Step 4: Choose `Elastic Beanstalk`, then `hello_phoenix` under Application name and then `Sample-env` under Environment name

Step 5: Choose `AWS-CodePipeline-Service` under Role name

Step 6: Review and click `Create pipeline`

Upon successful pipeline creation you will see that it is getting code from GitHub and deploying. Make some tea and wait.

## Verify deployment

In your AWS Elastic Beanstalk configuration console click on the URL next to the `Actions` button, it should look something like `http://sample-env.2j7f6imcis.us-west-2.elasticbeanstalk.com`

If your deployment was successful you will see default `Hello Phoenix` UI.
