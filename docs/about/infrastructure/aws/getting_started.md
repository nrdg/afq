# Getting started with Amazon Web Services (AWS)

Because many of the datasets that we would like to analyze are already in
Amazon's [S3](s3.md), we will use AWS for much of the computations we are doing.

## Interacting with AWS

There are several ways to interact with AWS.

### The web console

It's a website. You log in and click on buttons.

### The command-line interface (CLI)

To install the CLI use `pip install awscli` or `conda install -c conda-forge awscli`, or include
`awscli` in your environment configuration
(see also [documentation about Python package management](../installing_python_packages.md))

The first time that you use the CLI, you should run:

    aws configure

Provide your credentials (ask Ariel for credentials if you don't have these
yet). When asked about your preferred region, enter `us-east-1` and preferred
file format is `json`.

This will create two text files in `~/.aws/credentials` and `~/.aws/config`. You
can look at these files and even edit them, if you feel the need, but the CLI
should provide a safe way to do this.

#### Adding credentials

You will need to add credentials if you want to use multiple profiles in parallel.
For example, if you need to access data that is credentialed through the HCP

To add credentials for the HCP project (for example) use:

    aws configure --profile hcp

This will add a section to your `~/.aws/credentials` file with the access key id and 
secret access key that you got from the HCP for access to their data. Different 
credentials give you different priviliges. For example, the HCP credentials 
will only give you read access to the HCP OpenAccess Amazon S3 Bucket.



### Boto3

This is a Python library that allows you to interact with AWS. It is highly
useful, but the API can be a bit inconsistent and confusing.

[Documentation](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)

### S3FS

This library extends Boto3 to provide a *much nicer* and *more efficient*
interface to data stored in AWS S3.

[Documentation](https://s3fs.readthedocs.io/en/latest/)

### Cloudknot 

This library packages Python code for execution on AWS Batch.

[Documentation](https://nrdg.github.io/cloudknot)

### Jupyterhub 

We don't have one yet, but we will.
