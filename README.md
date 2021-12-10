# Azure Container Apps .NET Minimal API 

The following sample contains a simple .NET 6 minimal API.

It also contains a `Dockerfile` to build a valid .NET 6 docker container.

You can build and publish this container with `docker build -t <registry>/<image>:<version> .` and then `docker push ...` to push to a registry.

Then deploy to Azure Container Apps with a command line like the following (assumes an [Azure Container App environment]() has already been created for the $ACA_ENVIRONMENT property):

```bash
```