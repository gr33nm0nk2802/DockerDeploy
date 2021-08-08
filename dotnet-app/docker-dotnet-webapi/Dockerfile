# Stage 1
FROM mcr.microsoft.com/dotnet/sdk:5.0 as build
WORKDIR /app
COPY *.csproj ./
RUN dotnet restore
COPY . .
RUN dotnet publish -c Release -o out

# Stage 2
FROM mcr.microsoft.com/dotnet/aspnet
WORKDIR /app
COPY --from=build ./app/out .
ENTRYPOINT ["dotnet","docker-dotnet-webapi.dll"]