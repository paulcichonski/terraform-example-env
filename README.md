# terraform-example-env

Companion code for this blog post: [A Terraform Workflow Part 1: Packaging and
Versioning](https://medium.com/@paulcichonski/a-terraform-workflow-part-1-packaging-and-versioning-bc1fbbedecc6).

Serves as an example for how to build a static environment from the Docker image
created from [this repo](https://github.com/paulcichonski/terraform-workflow-example).

**Warning: this builds aws infrastructure, author is not responsible for AWS
**charges incurred**

## Guide for Building

This repo handles building a fictional staging environment.

First make sure you have the following environment variables exported:

* AWS_ACCESS_KEY_ID -> Your aws access key
* AWS_SECRET_ACCESS_KEY -> Your aws secret key
* REMOTE_BACKEND_S3_BUCKET -> a versioned s3 bucket in us-west-2. This will hold your Terraform state file.
* REMOTE_BACKEND_S3_KEY -> s3 key to use for Terraform state file name.

To build or update the environment:

```
## first run a plan to spot any issues
docker-compose run plan

## then apply changes
docker-compose run apply
```

To destroy the environment:

```
docker-compose run destroy
```

See `docker-compose.yml` for all supported commands.
