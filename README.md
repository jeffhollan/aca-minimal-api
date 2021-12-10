# Azure Container Apps .NET Minimal API 

The following sample contains a simple .NET 6 minimal API.

It also contains a `Dockerfile` to build a valid .NET 6 docker container.

You can build and publish this container with `docker build -t <registry>/<image>:<version> .` and then `docker push ...` to push to a registry.

Then deploy to Azure Container Apps with a command line like the following (assumes an [Azure Container App environment]() has already been created for the $ACA_ENVIRONMENT property):

```bash
az containerapp create \
    --name minimal-api \
    --resource-group $RESOURCE_GROUP \
    --environment $ACA_ENVIRONMENT \
    --image ghcr.io/jeffhollan/aca-minimal-api/app:main \
    --ingress 'external' \
    --target-port 80 \
    --query configuration.ingress.fqdn
```

#### Debug locally

After cloning and opening locally, you can run with:  

```bash
dotnet run
```