FROM mcr.microsoft.com/dotnet/sdk:10.0 AS build

WORKDIR /src

COPY DockerAPI.csproj ./

RUN dotnet restore

COPY . .

RUN dotnet publish -c Release -o out/publish

FROM mcr.microsoft.com/dotnet/aspnet:10.0 AS runtime

WORKDIR /app

COPY --from=build /src/out/publish .

EXPOSE 8080

CMD ["dotnet", "DockerAPI.dll"]