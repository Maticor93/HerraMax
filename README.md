# 📄 Documento de Requerimientos — Sistema de Gestión de Órdenes de Compra

**Cliente:** Ferretería Industrial “Herramax”  
**Fecha:** 08/08/2025  
**Solicitado por:** Departamento de Operaciones  

---

## 🎯 Objetivo del proyecto
La empresa necesita un sistema web que permita **gestionar órdenes de compra**, inventario y clientes de forma centralizada.  
Actualmente todo se maneja con **planillas Excel** y **correo electrónico**, lo cual genera errores, pérdida de información y demoras.

El sistema debe estar dividido en:
- **Backend:** Django REST Framework.
- **Frontend:** React.js.  

De forma que sea escalable y accesible desde cualquier dispositivo.

---

## 📦 Módulos requeridos

### 1. Gestión de Usuarios
- Registro y autenticación con email y contraseña.
- Roles de usuario:
  - **Administrador:** acceso total.
  - **Empleado:** puede ver y crear órdenes, pero no modificar usuarios.
- Recuperación de contraseña vía email.

### 2. Gestión de Clientes
- Alta, baja y modificación de clientes.
- Campos requeridos:
  - Nombre de la empresa / cliente.
  - Teléfono.
  - Email.
  - Dirección.
- Búsqueda y filtrado por nombre o email.

### 3. Gestión de Inventario
- Lista de productos con: código, nombre, descripción, precio y stock actual.
- Posibilidad de actualizar stock manualmente.
- Al generar una orden de compra, el stock debe descontarse automáticamente.

### 4. Gestión de Órdenes de Compra
- Crear nueva orden seleccionando cliente y productos.
- Cálculo automático del total.
- Estado de la orden: `Pendiente`, `En Proceso`, `Completada`, `Cancelada`.
- Listado y filtrado por estado y fecha.

### 5. Reportes
- Reporte mensual de ventas (total y por cliente).
- Exportar reportes en formato **CSV** o **PDF**.

---

## ⚙️ Requerimientos técnicos
- **Backend:** Django 5.x + Django REST Framework.
- **Frontend:** React 18 + Vite o CRA.
- **Base de datos:** PostgreSQL.
- Autenticación con JWT.
- Despliegue en servidor Linux (Ubuntu) con Nginx y Gunicorn.
- Uso de Git para control de versiones.

---

## 🎨 Requerimientos de UI/UX
- Diseño responsivo (PC, tablet, celular).
- Paleta de colores corporativos:
  - Azul: `#004080`
  - Gris: `#e6e6e6`
- Logo de la empresa en la barra de navegación.
- Navegación clara y minimalista.

---

## ⏳ Plazos
- **Fase 1:** Backend + API → 3 semanas.
- **Fase 2:** Frontend + integración API → 4 semanas.
- **Fase 3:** Pruebas y despliegue → 2 semanas.

---

## ✅ Criterios de aceptación
- Todas las funcionalidades descritas deben estar operativas.
- El sistema debe manejar correctamente casos de error (validaciones, mensajes claros).
- El tiempo de carga de páginas no debe superar los **2 segundos** en condiciones normales.
