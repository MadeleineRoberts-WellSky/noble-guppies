# Noble Guppies Demo Application

## Prerequisites

Install on Windows;

- [WSL 2](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
- [Docker with WSL 2 backend](https://docs.docker.com/docker-for-windows/wsl/)
- [VSCode](https://code.visualstudio.com/) with [Remote - WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) and [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker) extensions (required only for "Debugging" workflow)

Install on WSL:

- [Git](https://git-scm.com/download/linux)
- [.Net Core](https://docs.microsoft.com/en-us/dotnet/core/install/linux)

Clone this repository from within WSL:

```
git clone https://github.com/MadeleineRoberts-WellSky/noble-guppies.git

cd noble-guppies
```

## Running the Demo in VSCode

### Debugging with VSCode

Open cloned directory with VSCode:

```
code .
```

Press F5 to debug app.  VSCode will open a browser window.

### .Net Core CLI

To run from WSL command line or VSCode [Integrated Terminal](https://code.visualstudio.com/docs/editor/integrated-terminal) (without starting debugger):

```
dotnet run --project "./noble-guppies-demo/Noble Guppies.csproj"
```

Site will be running at https://localhost:5001/WeatherForecast.

### Docker

Run "Production" version in Docker:

```
docker-compose up
```

Site will be running at http://localhost:5000/WeatherForecast.

## Script to Create Project

This application was originally created in WSL 2 using the command line and VSCode.

```
# Create new .Net Core Wep API
dotnet new webapi --name "Noble Guppies" --output ./noble-guppies-demo

# Download .gitignore
wget -O .gitignore https://raw.githubusercontent.com/github/gitignore/master/VisualStudio.gitignore

# Open current directory with VSCode
code .
```

Press F5 (within VSCode) to create launch configuration (select .Net Core).  Add Docker-related files by pressing F1 and selecting "Docker: Add Docker Files to Workspace."
