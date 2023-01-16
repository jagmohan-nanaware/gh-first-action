1. Notes
   a. gh-first-action in github is cloned as github-actions

2. directory structure

   |--- README.txt
   |--- main.tf 
   |--- variable.tf
   |-+- cloudwatch-module
     |--- main.tf
     |--- version.tf


3. What is this code doing
   It is creating the following resources in the AWS infrastructure as follows
   a. cloudwatch_dashboard
      a dashboard of widgets created and customized to report on AWS metrics
   b. metric_alarm
      alarm takes one of more action based on the value of metric relative to a threshold
      over a range of time period 
   c. log_group
      collection of log_streams that share same monitoring and access control settings
   d. log_stream
      collection of log events that share the same resource


4. To create these resources using terraform in AWS
   a. change the directory to cloudwatch-module
   b. run terraform init
   c. run terraform plan
   d. run terraform apply

5. To check what has been created,
   a. go to AWS Console -> services -> CloudWatch
   b. clock on Dashboard, Log groups

6. Clean up using
   terraform destroy
