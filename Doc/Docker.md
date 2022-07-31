# Docker build

Download the artifact artifact.

Based on the dockerfile generated during the BuildService, generate a docker image.

Input parameters:
- DockerImage
- Registry

Secrets:
- CR_User
- CR_Password

The DockerImage is the name of the docker image in the container registry. The format is specific to the registry.  
For Azure Container Registry the format is {{ container name }}/{{ Solution Name }}:${{ github.event.inputs.serviceName }}_${{ github.event.inputs.version }}.${{ github.run_id }}-${{ github.run_number }} 
This means that all the services used in a solution are in this case stored in the same application directory with a name equal to the service and a tagging based on a version (Major.Minor.Patch), the run_id and run_number from github.  

The registry is the container registry identifier used to access it.


