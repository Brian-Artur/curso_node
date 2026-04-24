# Arquitectura principal

Fastify central  
   ↓  publica tarea  
RabbitMQ / Redis  
   ↓  
Workers Python  
   ↓  
resultado en BD / callback / evento  
   