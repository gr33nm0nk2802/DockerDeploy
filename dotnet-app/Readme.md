1. Install dotnet

```bash

# Updating packages
wget https://packages.microsoft.com/config/debian/10/packages-microsoft-prod.deb -O packages-microsoft-prod.deb
sudo dpkg -i packages-microsoft-prod.deb
rm packages-microsoft-prod.deb

# Install sdk
sudo apt-get update; \
  sudo apt-get install -y apt-transport-https && \
  sudo apt-get update && \
  sudo apt-get install -y dotnet-sdk-5.0

# Install runtime
sudo apt-get update; \
  sudo apt-get install -y apt-transport-https && \
  sudo apt-get update && \
  sudo apt-get install -y aspnetcore-runtime-5.0

sudo apt-get install -y dotnet-runtime-5.0  
```

2. Create a dotnet app

```bash
    dotnet new webApp -o docker-dotnet-app --no-https
```

or

```bash
    dotnet new webapi -o demo
```

3. Run the web app

```bash
    dotnet watch run

    #or
    
    dotnet dotnet-docker.dll
```

4. Create a docker file

```bash
    touch Dockerfile
```

5. Build a container

```bash
    docker build -t docker-app .
```

6. Run the container.

```bash
    docker run -p 80:80 docker-app
```
