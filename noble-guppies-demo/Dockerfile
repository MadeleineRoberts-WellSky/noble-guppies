FROM mcr.microsoft.com/dotnet/core/aspnet:3.1 AS base
WORKDIR /app
EXPOSE 5000

FROM mcr.microsoft.com/dotnet/core/sdk:3.1 AS build
WORKDIR /src
COPY ["noble-guppies-demo/Noble Guppies.csproj", "noble-guppies-demo/"]
RUN dotnet restore "noble-guppies-demo/Noble Guppies.csproj"
COPY . .
WORKDIR "/src/noble-guppies-demo"
RUN dotnet build "Noble Guppies.csproj" -c Release -o /app/build

FROM build AS publish
RUN dotnet publish "Noble Guppies.csproj" -c Release -o /app/publish

FROM base AS final
WORKDIR /app
COPY --from=publish /app/publish .
ENTRYPOINT ["dotnet", "Noble Guppies.dll"]
