# Azure Container Instances

 <a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FDaveAvid%2FIatse416-Deployment-Template%2Fmaster%2Fazuredeploy.json" target="_blank"> <img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true"/> </a>

This template demonstrates a simple use case for secret volumes of [Azure Container Instances](https://docs.microsoft.com/en-us/azure/container-instances/). When creating a container with the image containerinstance/helloworld:ssl, it sets up HTTP connections with the certificate and password passed in as secret volumes.

A PFX certificate is encoded in Base64 and mounted as a secret volume. Inside the container the certificate is accessible as a file with path /mnt/secrets/sslcertificateData. The password of the PFX certificate is also encoded in Base64, and mounted as a secret volume. Inside the container the certificate is accessible as a file with path /mnt/secrets/sslcertificatePwd.

The parameters sslcertificateData and sslcertificatePwd are only for demo purpose. Please create your own certificate when creating container groups.
