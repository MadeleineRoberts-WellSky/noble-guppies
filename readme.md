# Noble Guppies Demo Application

## Prerequisites

Install on Windows;

- [WSL 2](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
- [Docker with WSL 2 backend](https://docs.docker.com/docker-for-windows/wsl/)
- [VSCode](https://code.visualstudio.com/) with [Remote - WSL Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)

Install on WSL:

- [Git](https://git-scm.com/download/linux)
- [.Net Core](https://docs.microsoft.com/en-us/dotnet/core/install/linux)

Clone this repository from within WSL, and open with VSCode:

```
git clone https://github.com/MadeleineRoberts-WellSky/noble-guppies.git

code noble-guppies
```

## Running the Demo in VSCode

### Outside Docker

Press F5 to debug app.  VSCode will open a browser window.

To run from command line (without starting debugger):

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

```
# Create new .Net Core Wep API
dotnet new webapi --name "Noble Guppies" --output ./noble-guppies-demo

# Download .gitignore
wget -O .gitignore https://raw.githubusercontent.com/github/gitignore/master/VisualStudio.gitignore
```

Press F5 to create launch configuration (select .Net Core).
