# Arc4u.Guidance.Workflows

This project contains the github worflows to:
- Build an Arc4u micro-services
- Dockerize it
- Deploy it on AKS

The Arc4u Guidance generates a structure and the tool used are based on this structure.  
In this case, the naming is also following a strict rule and ease the build of a service and dockerize it.  

SolutionName: this is the name given to the solution (containing all the projects).  
ServiceName: each project in the solution is named and in the case of a micro-service, this is the name of the service.  

The folder structure is:  
.\BE\{{ ServiceName }}\{{ SolutionName }}.{{ ServiceName }}.Host\

The project's name is {{ ServiceName }}\{{ SolutionName }}.{{ ServiceName }}.Host.csproj

It is important to repect this structure because this is used by [BuildService.yml](Doc/BuildService.md)  
