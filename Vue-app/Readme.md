In this section we will create a simple production container for a vuejs app.

To create a base react app:

1. Install the requisites of nodejs, a text editor and vetur extention.

2. Vue js can be included into our project in multiple ways,

    - By using a CDN package
    - npm 

```bash
    npm install vue@next 
```

    - vue CLI (prefered)

```bash
    npm install -g @vue/cli @vue/cli-service-global
    vue create docker-vuejs-app
```

    - Vite

```bash
    npm init vite-app <project-name>
```

2. Move inside of the `docker-vuejs-app` and build the production app

```bash
    cd docker-vuejs-app
    npm run build
```

3. Create a Dockerfile for production

```bash
    touch Dockerfile
```

4. Run docker build

```bash
    docker build -t vuejs-app .
```

5. Run the container locally

```bash
    docker run -p 80:80 vuejs-app
```