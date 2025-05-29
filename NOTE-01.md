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

