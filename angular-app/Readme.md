To create an production angular app we have to do it in two stages.

1. Install node

2. Install `@angular/cli` globally

```bash
    npm install -g @angular/cli
```

3. Create a new angular app.

```bash
    ng new docker-angular-app
```

4. Build the angular app by first changing the build script or adding a new script `ng build --prod`.

```bash
    ng build
```

5. Create a Dockerfile

```bash
    touch Dockerfile
```

6. Build the docker image.

```bash
    docker build -t angular-app .
```

7. Run the docker container.

```bash
    docker run -p 80:80 angular-app
```