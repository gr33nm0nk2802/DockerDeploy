In this section we will create a simple production container for a Nestjs app.

To create a base Nestjs app:

1. Install Nestjs globally and create an app.

```bash
    npm i -g @nestjs/cli
    nest new docker-nest-app
```

2. Move inside of the `docker-nest-app` and build the production app

```bash
    cd docker-nest-app
    npm run build
```

3. Create a Dockerfile for production

```bash
    touch Dockerfile
```

4. Run docker build

```bash
    docker build -t nest-container .
```

5. Run the container locally

```bash
    docker run -p 80:80 nest-container
```