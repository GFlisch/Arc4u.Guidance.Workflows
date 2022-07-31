# Build Service

Build a .NET Arc4u service and save it in an artifact.
Don't run any test or Sonarqube analyzis.

Will be used by another workflow (Docker) to build a docker image and save it to a container registry.

Produce the Docker file for Docker.

Result is in an artifact named artifact

./Service     => contains the release build.
./Dockerfile  => the Docker file to build a docker image.
./deploy.yml  => the file to deploy the service in a k8s environment.

No secrets are needed.

Input parameters:
- solutionName: The name of the Solution.
- serviceName: The name of the micro-service.
- dotNet: The version if the .Net runtime 6.0 or 6. The workflow will add a .*!

