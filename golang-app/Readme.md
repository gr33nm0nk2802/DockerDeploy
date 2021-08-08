
1. Initialize the `go mod`.

```bash
    go mod init docker-golang-app
```

2. Create a main.go file with the following code.

```go

package main

import "github.com/gofiber/fiber/v2"

func main() {
    app := fiber.New()

    app.Get("/", func(c *fiber.Ctx) error {
        return c.SendString("Hello, World 👋!")
    })

    app.Listen(":3000")
}

```

3. Go get the fiver module

```bash
    go get github.com/gofiber/fiber/v2
```

4. Create a Dockerfile

```bash
   touch Dockerfile
```

5. Build the container

```bash
    docker build -t docker-golang-app .
```

6. Run the container

```bash
    docker run -p 80:80 docker-golang-app
```


