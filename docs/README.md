# Índece

+ [Arquitectura deseada](./01_arquitectura_deseada.md)
+ [Herramientas](./02_herramientas.md)
+ [Libuv](./03_libuv.md)
+ [File System](./04_file_system.md)
+ [Componentes](./05_componentes.md)
+ [Iniciar proyecto nuevo](./06_iniciar_proyecto.md)


# Completado
## 1. Base del proyecto
+ [ ] Crear proyecto Node + TypeScript 
+ [ ] Configurar tsconfig
+ [ ] Usar ESM o CommonJS de forma consciente
+ [ ] Configurar scripts: dev, build, start
+ [ ] Usar variables de entorno con .env
+ [ ] Crear estructura inicial por carpetas

```
src/
 ├─ modules/
 ├─ shared/
 ├─ config/
 ├─ server.ts
 └─ main.ts
 ```

## 2. Fastify básico
+ [ ] Crear servidor Fastify
+ [ ] Crear rutas GET, POST, PUT, DELETE
+ [ ] Entender request, reply y return
+ [ ] Separar rutas por módulos
+ [ ] Registrar plugins
+ [ ] Manejar prefijos: /api/users, /api/products

## 3. TypeScript + OOP
+ [ ] Crear controllers como clases
+ [ ] Crear services como clases
+ [ ] Crear repositories como clases
+ [ ] Usar interfaces
+ [ ] Aplicar inyección de dependencias sencilla
+ [ ] Separar responsabilidades

Ejemplo mental:

UserController → recibe HTTP
UserService    → lógica de negocio
UserRepository → acceso a base de datos

## 4. Validación de datos
+ [ ] Validar body
+ [ ] Validar params
+ [ ] Validar query params
+ [ ] Crear DTOs
+ [ ] Usar Zod o TypeBox
+ [ ] Devolver errores claros si los datos son incorrectos


5. Errores y respuestas
[ ] Crear errores personalizados
[ ] Manejar errores globales
[ ] Unificar formato de respuesta
[ ] Diferenciar errores 400, 401, 403, 404, 500

Ejemplo:

NotFoundError
ValidationError
UnauthorizedError
6. Base de datos MongoDB
[ ] Conectar Fastify con MongoDB
[ ] Crear modelos/esquemas
[ ] Hacer CRUD básico
[ ] Separar Mongo en repositories
[ ] Manejar errores de conexión

Aquí podrías usar Mongoose si quieres algo más guiado.

7. Base de datos PostgreSQL
[ ] Conectar PostgreSQL
[ ] Crear tablas
[ ] Hacer CRUD básico
[ ] Entender migraciones
[ ] Usar relaciones simples
[ ] Separar queries/repositorios

Aquí podrías usar Prisma o Drizzle.

## 8. Autenticación
+ [ ] Registro de usuarios
+ [ ] Login
+ [ ] Hash de contraseñas
+ [ ] JWT
+ [ ] Middleware de autenticación
+ [ ] Rutas protegidas
+ [ ] Roles básicos: admin/user

## 9. Documentación de API
[ ] Documentar endpoints
[ ] Añadir ejemplos de request/response
[ ] Usar Swagger/OpenAPI
[ ] Crear una colección de Postman o Bruno

## 10. Docker básico
+ [ ] Crear Dockerfile para la API
+ [ ] Crear docker-compose
+ [ ] Levantar API + MongoDB
+ [ ] Levantar API + PostgreSQL
+ [ ] Usar variables de entorno en Docker

## 11. Redis / caché
+ [ ] Conectar Redis
+ [ ] Guardar datos temporales
+ [ ] Leer datos desde caché
+ [ ] Invalidar caché
+ [ ] Usar expiración con TTL

Ejemplo:

/products → primero mira Redis → si no hay datos, consulta PostgreSQL
## 12. Testing con Vitest
+ [ ] Testear funciones simples
+ [ ] Testear services
+ [ ] Testear repositories con mocks
+ [ ] Testear endpoints con fastify.inject()
+ [ ] Testear errores
+ [ ] Crear tests de integración básicos