# deno-typescript-template

- Use `Deno.env.get("PORT")` in your serving function.

```typescript
import { serve } from "https://deno.land/std@0.140.0/http/server.ts";

function handler(_req: Request): Response {
  return new Response("Hello World!");
}

serve(handler, { port: Deno.env.get("PORT") });
```

- Create a file `deno.json` and add the starting command.

```json
{
  "tasks": {
    "start": "deno run --allow-net --allow-env --allow-read main.ts"
  }
}

```

- To run locally, copy `.env.defaults` to a new file `.env`, and modify `.env` by assigning the port that you would like to run your application.

    ```shell
    cp .env.defaults .env
    ```

    ```shell
    # in .env
    PORT=<your port>
    ```
