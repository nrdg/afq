# How to use AWS in our projects

## Getting credentials

We try to use the [principle of least privilege](https://en.wikipedia.org/wiki/Principle_of_least_privilege). 
That means that when you get credentials to access our AWS account, we will try to limit your 
privileges as much as possible, so that you can still do the things you need to do with your 
AWS account. This ensures that you don't accidentally do things you don't need to do that 
can affect others (e.g., deleting data you are not working with, or starting machines when you 
don't need to do that). 

### Compromised credentials

Compromised credentials are credentials that may have been exposed to people who should not have them. 
One (scarily common) way in which credentials can get compromised is if they are somehow stored in 
code and get committed to a repository and pushed to GitHub. Please note that if you committed credentials 
into the history of a git repo, they will still be there in the history of the repo, 
*even if you delete them and commit the deletion*. This means that if you committed the credentials, and you 
are not sure how to remove them from the repo history, do not push that repo to GitHub, and ask for 
someone to help.

We hope to never have compromised credentials, but if you have reason to believe that your credentials were 
compromised (e.g., you accidentally pushed them to GitHub), please let us know as soon as possible, so that 
we can mitigate the potential harm of this.

### Multi-factor authentication

If your credentials allow you to log into the AWS console, you *must* use multi-factor 
authentication. MFA means that in addition to entering your password when logging in, 
another form of authentication will be required to get access to the console. For example, 
a cell-phone app that provides you with a token. 

## Rules of thumb for resource usage

### Always tag resources with a "project" tag

Tagging resources helps us track how much resources are being used in what project.
Tagging is easy if you are using the console. Whenever starting a resource (e.g., 
EC2 instance, or S3 bucket, you will have the option to tag it through the console).

We currently have the following tags:

- HCP 
- HBN
- ABCD
- IXI
- dHCP

### Consider how you are using storage 

Block storage (for example an EC2 instance hard-drive) is about an order of magnitude more expensive than 
an Amazon Machine Image, which is about an order of magnitude more expensive than highly-available S3, which is 
about an order of magnitude more expensive than Glacier storage. 

### Use the smallest possible instance for the job

Similar to storage, please consider what machine you are using. When launching an EC2 instance from the console, 
pay attention to the RAM and CPU that are provided by the instance that you are using and choose the smallest 
amount of these that will let you comfortably do the work you want to do. Similarily

### When in doubt, ask someone 

If you think that what you are about to do will cost less than $50, go ahead and do it (As an example, 
preprocessing with qsiprep/cloudknot on spot instances costs about $1/participant). If you think that it would 
cost  $50 - $1,000, please post to the `#AWS` slack channel, and wait for someone else to provide feedback. If 
you are interested in doing something really ambitious that you think will cost more than $1,000, please ask 
Ariel (he'll probably say "go ahead").

You can calculate usage/cost with the [AWS cost calculator](https://calculator.aws/#/).