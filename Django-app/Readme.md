
1. 

```
pip install django
```

2.

```
django-admin startproject dockerDjangoApp
```

3. Change directory into `dockerDjangoApp`

4. Create a requirements file and Dockerfile.

5. Build the container

```
docker build -t django-app .
```

6. Run the container

```
docker run -p 80:80 django-app
```

