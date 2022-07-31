# Build Service

Build a DOTNET Arc4u service and save it in an artifact.
Don't run any test or Sonrqube analyzis.

Will be used by another workflow (Docker) to build a docker image and save it to a container registry.

Produce the Docker file for Docker.

Result is in an artifact named artifact

./Service     => contains the release build.
./Dockerfile  => the Docker file to build a docker image.
./deploy.yml  => the file to deploy the service in a container.

No secrets are needed.

