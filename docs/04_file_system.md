# Qué es fs  

Es un módulo interno de Node que sirve para trabajar con archivos y carpetas.

Tiene acceso a los archivos que el usuario del sistema que ejecuta Node tenga 
permiso para leer o escribir.

```
/home/tu_usuario/proyecto/README.md  ✅
/etc/passwd                         quizá lectura ✅
/root/archivo.txt                   normalmente ❎
```

# Importación
```js
const fs = require('fs');             // CommonJS
import fs from 'node:fs';             // ESM
```