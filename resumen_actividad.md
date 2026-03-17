
# Sistema de Subastas – Resumen del Trabajo

## Objetivo del proyecto
Desarrollar una **aplicación móvil** conectada a un **backend con API REST** que permita:

- Participar en **subastas online en tiempo real**
- Publicar objetos para que la empresa los subaste
- Gestionar usuarios y medios de pago
- Integrarse con el sistema existente de la empresa

La empresa ya posee un sistema interno, por lo que la app deberá **consumir y actualizar información mediante APIs**.

---

# Tipos de usuarios

## 1. Postor (usuario)
Puede:

- Registrarse
- Ver subastas
- Participar pujando
- Comprar objetos
- Ver historial y estadísticas
- Proponer objetos para subastar

## 2. Dueño de objetos
Puede:

- Proponer artículos para subasta
- Ver si fueron aceptados o rechazados
- Ver seguro y ubicación del objeto
- Cobrar cuando se vende

## 3. Empresa
Se encarga de:

- Verificar usuarios
- Aceptar o rechazar objetos
- Organizar subastas
- Registrar ventas
- Gestionar seguros y pagos

---

# Registro de usuarios

El registro tiene **dos etapas**.

## Etapa 1 – Registro inicial

El usuario ingresa:

- Nombre
- Apellido
- Foto del documento (frente y dorso)
- Domicilio legal
- País de origen

La empresa verifica los datos y asigna una **categoría**:

- Común
- Especial
- Plata
- Oro
- Platino

La categoría determina **a qué subastas puede acceder**.

---

## Etapa 2 – Activación

El usuario:

- Crea su contraseña
- Registra **medios de pago**

Debe tener **al menos uno verificado** para poder participar en subastas.

Medios de pago posibles:

- Cuenta bancaria
- Tarjeta de crédito
- Cheque certificado

---

# Subastas

Cada subasta tiene:

- Fecha
- Hora
- Ubicación
- Categoría mínima requerida
- Rematador
- Moneda (ARS o USD)
- Catálogo de objetos

Los usuarios solo pueden participar si:

- Están registrados
- Su categoría es suficiente
- Tienen al menos un medio de pago verificado

Un usuario **solo puede estar conectado a una subasta a la vez**.

---

# Objetos del catálogo

Cada objeto tiene:

- Número de pieza
- Descripción
- Precio base
- Dueño actual
- Imágenes (aprox. 6)

Si es arte o diseño también incluye:

- Artista o diseñador
- Fecha
- Historia del objeto

---

# Pujas (ofertas)

Las ofertas deben cumplir ciertas reglas.

## Puja mínima

Debe ser:

```
última oferta + 1% del precio base
```

Ejemplo:

Precio base = 10.000  
Última oferta = 15.000  

Puja mínima = **15.100**

---

## Puja máxima

Debe ser:

```
última oferta + 20% del precio base
```

Ejemplo:

Máximo = **17.000**

⚠️ Esta restricción **no aplica para subastas Oro o Platino**.

---

# Tiempo real

Los usuarios deben recibir en tiempo real:

- Nuevas ofertas
- Cambios de precio
- Estado de la subasta

Esto permite reaccionar rápidamente y hacer nuevas pujas.

---

# Finalización de la subasta

Cuando nadie supera la última oferta:

- El último postor **gana el objeto**
- Se registra la venta
- Se asigna el nuevo dueño
- Se calculan comisiones
- Se calcula el envío

El usuario recibe un mensaje con:

- Precio final
- Comisiones
- Costo de envío

---

# Pago

Si el usuario no paga:

1. Recibe una **multa del 10% del valor ofertado**
2. Tiene **72 horas para pagar**

Si no cumple:

- Se inicia proceso judicial
- El usuario queda bloqueado en la aplicación

---

# Métricas del usuario

La app debe mostrar estadísticas como:

- Subastas en las que participó
- Subastas ganadas
- Historial de pujas
- Dinero ofertado
- Dinero pagado

---

# Proponer objetos para subasta

Los usuarios pueden enviar objetos para vender.

Datos requeridos:

- Descripción
- Fotos (mínimo 6)
- Historia del objeto
- Declaración de propiedad
- Declaración de origen lícito

---

# Proceso de aceptación

1. Usuario envía la solicitud
2. Empresa solicita el envío del objeto
3. Empresa inspecciona el objeto

La empresa puede:

- **Aceptar**
- **Rechazar**

Si lo acepta:

- Se incluye en una futura subasta
- Se define precio base
- Se definen comisiones

El usuario puede **aceptar o rechazar estas condiciones**.

---

# Seguro

Cada objeto aceptado tiene un seguro.

El dueño puede ver:

- La póliza
- La ubicación del objeto
- El depósito donde se encuentra

También puede **aumentar el valor del seguro pagando la diferencia**.

---

# Envíos

Cuando un objeto se vende:

- El comprador paga el envío
- El costo aparece en la factura

También puede **retirarlo personalmente**, pero pierde cobertura del seguro.

---

# Streaming

La empresa provee un **servicio de streaming** para ver la subasta.

⚠️ Este servicio **no forma parte del desarrollo**, solo se accede desde la app.

---

# Entregables del trabajo

## Primera entrega

- Wireframes de la app (mínimo 5 en alta definición)
- Paleta de colores
- Icono de la app
- Pantalla splash
- Plano en Figma
- Diseño del **API REST** (Swagger)

Ejemplos de endpoints:

```
POST /login
GET /subastas
GET /subastas/{id}
POST /pujas
GET /catalogo
```

Incluyendo:

- Parámetros
- Respuestas
- Códigos HTTP

---

## Segunda entrega

Aplicación funcionando al **50%**:

- Backend implementado
- Frontend implementado
- Conexión entre ambos
- Al menos un flujo completo funcionando

Ejemplo:

```
login → ver subastas → entrar a subasta → pujar
```

También debe incluir:

- Manejo de errores
- Validaciones
- Manejo de conexión a internet

---

## Tercera entrega

Aplicación **100% funcional**:

- Backend deployado en internet
- Endpoints accesibles
- Frontend instalable en un dispositivo móvil

---

# Resumen final

El proyecto consiste en desarrollar una **app móvil de subastas en tiempo real** con:

- Registro y verificación de usuarios
- Gestión de medios de pago
- Catálogo de subastas
- Sistema de pujas en tiempo real
- Compra de objetos
- Gestión de envíos
- Métricas de participación
- Publicación de objetos para subastar
