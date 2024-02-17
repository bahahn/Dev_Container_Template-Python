# Dev_Container_Template (Python)
The project Dev_container_Template (Python) should serve as a template for development in a Python container. The aim is to introduce as little additional work as possible into the development process. <br>
A normal Dockerfile with Docker-Compose is required for use. An additional service ("dev container") is created in the Docker-Compose. This can be started by integrating it into an editor (e.g. Visual Studio Code) using the settings in the devcontainer.json file. <br>
A pipfile is read into the Dockerfile, which installs the required libraries.

## Requirements
- Supporter Editor (e.g. Visual Studio)
- Dev Container extension (VS Code)
- Docker (for obvious reasons)
- Docker extension (VS Code)


## How To (VS Code)
- Navigate to the template
- Open the command palette
- Select Dev Containers: Reopen in Container
 
