# Pasos crear proyecto Fastify

1. Crear proyecto
   ```bash
   mkdir fastify-ts-lab                         # Carpeta del proyecto
   cd fastify-ts-lab`
   npm init -y`                                 # Crear package.json
   ```

2. `npm install fastify` : Instalar dependencias
   `npm install -D typescript @types/node tsx rimraf`
   - fastify      → framework backend
   - typescript   → compilador TS
   - @types/node  → tipos de Node.js
   - tsx          → ejecutar TS en desarrollo
   - rimraf       → borrar dist antes de compilar

3. `npx tsc --init --rootDir src --outDir dist` : Crear tsconfig.json
   Configurar tsconfig:
   ```json
   {
     "compilerOptions": {
       "target": "ES2022",
       "module": "NodeNext",
       "moduleResolution": "NodeNext",
       "rootDir": "src",
       "outDir": "dist",
       "strict": true,
       "esModuleInterop": true,
       "skipLibCheck": true
     },
     "include": ["src"]
   }
   ```

4. Configurar package.json : 
   ```json
   {
     "type": "module",
     "scripts": {
       "dev": "tsx watch src/main.ts",          // dev recarga automática
       "typecheck": "tsc --noEmit",             // revisar errores de TS
       "build": "rimraf ./dist && tsc",         // Compilar a JS
       "start": "node dist/main.js"             // Ejecutar versión JS
     }
   }
   ```

5. Crear estructura inicial
   ```
   src/
   ├─ app.ts
   └─ main.ts
   ```
   1. Crear src/app.ts
      ```ts
      import { buildApp } from "./app.js"

      const app = buildApp()

      try {
        await app.listen({
          port: 3000,
          host: "0.0.0.0"
        })
      } catch (error) {
        app.log.error(error)
        process.exit(1)
      }
      ```
   2. Crear src/main.ts
      ```ts
      import { buildApp } from "./app.js"

      const app = buildApp();

      try {
        await app.listen({
          port: 3000,
          host: "0.0.0.0"
        })
      } catch (error) {
        app.log.error(error)
        process.exit(1)
      }
      ```
6. `npm run dev` : Ejecutar en desarrollo → http://localhost:3000
7. `npm run typecheck` : Revisar tipos
8. `npm run build && npm run start` : Compilar y ejecutar producción
  
  