1. Install deno onto the system

```bash
    curl -fsSL https://deno.land/x/install/install.sh | sh
```
2. Write the `app.ts` file

```bash
import { serve } from "https://deno.land/std@0.103.0/http/server.ts";
const s = serve({ port: 8000 });
console.log("http://localhost:8000/");
for await (const req of s) {
  req.respond({ body: "Hello World\n" });
}
```

3. Run the app

```bash
    deno run --allow-net app.ts
```

4. Create a Dockerfile

```bash
    touch Dockerfile
```

5. Build the container

```bash
    docker build -t deno-app .
```

6. Run the container

```bash
    docker run -p 80:80 deno-app
```