
# Roadmap de Desarrollo – App Sistema de Subastas

Este roadmap organiza el trabajo para completar el proyecto en **3 etapas (entregas)** asegurando que el equipo llegue a tiempo.

---

# Visión general

Etapas del proyecto:

1. **Diseño y definición (Primera entrega)**
2. **Desarrollo inicial funcional (Segunda entrega)**
3. **Sistema completo y deploy (Tercera entrega)**

---

# Fase 1 — Análisis y Diseño (Primera entrega)

Objetivo: Definir cómo será la app antes de programar.

## 1. Entender requerimientos
- Leer completamente la consigna
- Identificar actores del sistema
- Identificar funcionalidades principales
- Definir casos de uso principales

Checklist:

- [ ] Identificar tipos de usuario
- [ ] Definir funcionalidades principales
- [ ] Definir reglas de pujas
- [ ] Definir restricciones de subastas

---

## 2. Definir arquitectura

Decidir tecnologías:

- Frontend móvil
- Backend
- Base de datos
- Comunicación en tiempo real

Ejemplo:

- Frontend: React Native / Flutter / Vue + Capacitor
- Backend: Node.js / Java / Python
- Base de datos: PostgreSQL / MySQL
- Tiempo real: WebSockets

Checklist:

- [ ] Elegir stack tecnológico
- [ ] Definir arquitectura cliente-servidor
- [ ] Definir comunicación en tiempo real

---

## 3. Diseñar base de datos

Entidades principales:

- Usuarios
- Medios de pago
- Subastas
- Objetos
- Pujas
- Ventas
- Seguros
- Catálogo

Checklist:

- [ ] Diagrama entidad-relación
- [ ] Definir relaciones
- [ ] Definir claves primarias
- [ ] Definir restricciones

---

## 4. Diseñar API REST

Definir endpoints principales:

Usuarios

- POST /register
- POST /login
- GET /profile

Subastas

- GET /subastas
- GET /subastas/{id}

Pujas

- POST /pujas
- GET /pujas/{subasta}

Objetos

- POST /objetos
- GET /objetos/{id}

Checklist:

- [ ] Documentar endpoints
- [ ] Definir parámetros
- [ ] Definir respuestas
- [ ] Definir códigos HTTP
- [ ] Generar documentación Swagger

---

## 5. Diseñar interfaz (UI / UX)

Crear wireframes de pantallas.

Pantallas mínimas recomendadas:

1. Login
2. Registro
3. Lista de subastas
4. Detalle de subasta
5. Pantalla de pujas
6. Catálogo de objetos
7. Perfil de usuario
8. Agregar medio de pago
9. Subir objeto a subasta

Checklist:

- [ ] Wireframes baja fidelidad
- [ ] Wireframes alta fidelidad
- [ ] Definir paleta de colores
- [ ] Diseñar icono de app
- [ ] Diseñar pantalla splash
- [ ] Crear proyecto en Figma

---

# Fase 2 — Desarrollo Inicial (Segunda entrega)

Objetivo: Tener el **50% del sistema funcionando**.

---

## 1. Backend básico

Implementar:

- Autenticación
- Gestión de usuarios
- Gestión de subastas
- Gestión de objetos

Checklist:

- [ ] Configurar servidor backend
- [ ] Implementar login
- [ ] Implementar registro
- [ ] Endpoint listado de subastas
- [ ] Endpoint detalle subasta

---

## 2. Base de datos

Implementar tablas.

Checklist:

- [ ] Tabla usuarios
- [ ] Tabla medios_pago
- [ ] Tabla subastas
- [ ] Tabla objetos
- [ ] Tabla pujas
- [ ] Tabla ventas

---

## 3. Frontend inicial

Implementar pantallas básicas.

Checklist:

- [ ] Pantalla login
- [ ] Pantalla registro
- [ ] Pantalla lista subastas
- [ ] Pantalla detalle subasta
- [ ] Pantalla perfil usuario

---

## 4. Conexión frontend-backend

Primer flujo completo funcionando.

Flujo recomendado:

login → ver subastas → entrar a subasta → ver ofertas

Checklist:

- [ ] Consumir API desde frontend
- [ ] Manejar autenticación
- [ ] Mostrar datos de subastas

---

## 5. Manejo de errores

Implementar validaciones.

Checklist:

- [ ] Campos obligatorios
- [ ] Validación de formularios
- [ ] Manejo de errores API
- [ ] Manejo de conexión a internet

---

# Fase 3 — Funcionalidades completas (Tercera entrega)

Objetivo: Sistema completamente funcional.

---

## 1. Sistema de pujas en tiempo real

Implementar:

- WebSockets o similar
- Actualización en vivo

Checklist:

- [ ] Conexión en tiempo real
- [ ] Mostrar nuevas pujas
- [ ] Validar pujas en backend

---

## 2. Gestión de pagos

Implementar:

- Registro medios de pago
- Verificación
- Límite por fondos garantizados

Checklist:

- [ ] Crear medios de pago
- [ ] Validar medios antes de pujar

---

## 3. Venta final

Implementar lógica:

- Determinar ganador
- Registrar venta
- Calcular comisiones
- Calcular envío

Checklist:

- [ ] Registrar venta
- [ ] Asignar nuevo dueño
- [ ] Generar detalle de pago

---

## 4. Subir objetos para subasta

Permitir a usuarios:

- Cargar objetos
- Subir fotos
- Declarar propiedad

Checklist:

- [ ] Formulario carga objeto
- [ ] Subida de imágenes
- [ ] Registro de solicitud

---

## 5. Métricas del usuario

Implementar:

- Historial de subastas
- Subastas ganadas
- Historial de pujas

Checklist:

- [ ] Endpoint estadísticas
- [ ] Pantalla historial usuario

---

## 6. Deploy

Publicar sistema.

Checklist:

Backend

- [ ] Deploy en servidor
- [ ] API accesible online

Frontend

- [ ] Build aplicación
- [ ] Instalar en dispositivo móvil

---

# Checklist final del proyecto

Antes de entregar:

- [ ] Todas las pantallas funcionan
- [ ] Backend accesible
- [ ] API documentada
- [ ] Wireframes entregados
- [ ] App instalable
- [ ] Flujo completo probado

---

# Resultado esperado

Una **aplicación móvil funcional de subastas online** que permita:

- Participar en subastas en tiempo real
- Pujar por objetos
- Comprar artículos
- Publicar objetos para subasta
- Ver estadísticas y actividad
