# terraform-example-env

Companion code for this blog post: TODO: LINK

Serves as an example for how to build a static environment from the Docker image
created from [this repo](https://github.com/paulcichonski/terraform-example).

**Warning: this builds aws infrastructure, author is not responsible for AWS
**charges incurred**

## Guide for Building

This repo handles building a fictional staging environment.

To build or update the environment:

```
docker-compose run apply
```

To destroy the environment:

```
docker-compose run destroy
```

See `docker-compose.yml` for all supported commands.
