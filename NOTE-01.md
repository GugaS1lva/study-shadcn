Ready to Code!

Instalar Tailwind v4 + Vite.js:
```bash
npm create vite@latest
```

```bash
npm install tailwindcss @tailwindcss/vite
```

```bash
vite.config.ts

    import { defineConfig } from 'vite'
>>> import tailwindcss from '@tailwindcss/vite'
    export default defineConfig({
      plugins: [
>>>     tailwindcss(),
      ],
    })
```

```bash
global.css

@import "tailwindcss";
```

```bash
main.tsx

import './global.css'
```

Instalar Shadcn-UI - [ Siga os passos acima também. ]

```bash
tsconfig.json

{
  "files": [],
  "references": [
    {
      "path": "./tsconfig.app.json"
    },
    {
      "path": "./tsconfig.node.json"
    }
  ],
> "compilerOptions": {
>   "baseUrl": ".",
>   "paths": {
>     "@/*": ["./src/*"]
>   }
> }
}
```

```bash
tsconfig.app.json

{
  "compilerOptions": {
    // ...
>   "baseUrl": ".",
>   "paths": {
>     "@/*": [
>       "./src/*"
>     ]
>   }
    // ...
  }
}
```

```bash
npm install -D @types/node
```

```bash
vite.config.ts

> import path from "path"
> import tailwindcss from "@tailwindcss/vite"
  import react from "@vitejs/plugin-react"
  import { defineConfig } from "vite"
  
  // https://vite.dev/config/
  export default defineConfig({
>   plugins: [react(), tailwindcss()],
>   resolve: {
>     alias: {
>       "@": path.resolve(__dirname, "./src"),
>     },
>   },
  })
```

```bash
npx shadcn@latest init
```

```bash
npx shadcn@latest add button
npx shadcn@latest add button table dialog 
```