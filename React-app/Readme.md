In this section we will create a simple production container for a react app.

To create a base react app:

1. Create a react app using npx

```bash
    npx create-react-app docker-react-app
```

2. Move inside of the `docker-react-app` and build the production app

```bash
    cd docker-react-app
    npm run build
```

3. Create a Dockerfile for production

```bash
    touch Dockerfile
```

4. Run docker build

```bash
    docker build -t react-container .
```

5. Run the container locally

```bash
    docker run -p 80:80 react-container
```