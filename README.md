# Arc4u.Guidance.Workflows

This project contains the github reusable worflows to:
- Build an Arc4u micro-services or a Blazor web Assembly
- Dockerize it
- Deploy it on AKS

The Arc4u Blueprint generates a structure and the tool used are based on this structure.  
In this case, the naming is also following a strict rule and ease the factorization to build a service and dockerize it.  

## Deploy a Aspnet core web api.

SolutionName: this is the name given to the solution (containing all the projects).  
ServiceName: each project in the solution is named and in the case of a micro-service, this is the name of the service.  

The folder structure is:  
.\\BE\\{{ ServiceName }}\\{{ SolutionName }}.{{ ServiceName }}.Host\\

The project's name is {{ SolutionName }}.{{ ServiceName }}.Host.csproj

It is important to repect this structure because this is used by [BuildService.yml](Doc/BuildService.md)  

## Deploy a Blazor WebAssembly.

SolutionName: this is the name given to the solution (containing all the projects).  
BlazoreName: Name of the Blazor app. 

The folder structure is:  
.\\FE\\{{ BlazoreName }}\\{{ SolutionName }}.{{ BlazoreName }}\\

The project's name is {{ SolutionName }}.{{ BlazoreName }}.csproj