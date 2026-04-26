# Librerías Node
+ Fastify : recibir peticiones HTTP
+ Pino : logger con muy baja sobrecarga
  `npm i pino`
+ Axios : enviar peticiones HTTP
  `React → Fastify → Axios → microservicio`
+ UUID : generar identificadores únicos
  `550e8400-e29b-41d4-a716-446655440000`
+ amqplib : comunicarse con RabbitMQ

# Containers
+ nginx
→ reverse proxy, HTTPS, dominios, redirecciones

+ frontend-react
→ aplicación visible para el usuario

+ api-fastify-main
→ backend principal, lógica de negocio, auth, endpoints

+ postgresql
→ base de datos relacional principal

+ mongodb
→ base de datos documental si la necesitas

+ redis
→ caché, sesiones, rate limit, datos temporales

+ rabbitmq
→ colas de tareas y comunicación asíncrona

+ worker-emails
→ envía emails en segundo plano

+ worker-pdfs
→ genera PDFs, facturas, documentos

+ worker-automations
→ procesos programados, tareas internas, integraciones

+ minio
→ almacenamiento tipo S3 para archivos, imágenes, PDFs

+ prometheus
→ recoge métricas

+ grafana
→ panel visual de métricas

+ loki
→ logs centralizados

+ backup-service
→ copias de seguridad de BD y archivos

+ portainer
→ panel visual para gestionar Docker

+ watchtower
→ actualiza contenedores automáticamente