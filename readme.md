# Noble Guppies Demo Application

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

Press F5 to create launch configuration (select .Net Core).  Will be running at https://localhost:5001/WeatherForecast.
