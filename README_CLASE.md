# Casos desarrollado en clase 

---

## 1. Portada

| Campo | Detalle |
|---|---|
| **Nombre completo** | *VILA CAYO NAYHERLY DIANETH* |
| **Código universitario** | *27202120* |
| **Curso** | S489 — Pruebas y Aseguramiento de Calidad de Software |
| **Docente** | Ing. Lizbeth Jaico |
| **Sistema elegido** | InkaRetail|
| **Módulo analizado** | Login / Registro |
| **Universidad** | Universidad Nacional de San Cristóbal de Huamanga |
| **Fecha** | Mayo 2026 |

---

## 2. Descripción del sistema bajo prueba

InkaRetail S.A.C. es una empresa de retail con 12 tiendas en Ayacucho, Huancayo y Cusco que está desarrollando el SGI (Sistema de Gestión de Inventario), una aplicación web que permite a los usuarios autenticarse, acceder al inventario de productos y gestionar el stock de cada tienda. El sistema ofrece funcionalidades como inicio de sesión seguro con roles (Administrador, Vendedor, Jefe de Almacén), registro de nuevos usuarios con validación de contraseña, consulta y actualización de stock, generación de alertas por stock bajo y emisión de reportes. Cuenta con validaciones de negocio en todos los formularios, proporcionando una experiencia segura y accesible desde cualquier navegado

---

## 3.  Módulo elegido y justificación

### Módulo: Login y Registro

Se eligió el módulo de **Login y Registro** por las siguientes razones:

- **Es la puerta de entrada al sistema.** Sin autenticación correcta, el usuario no puede acceder a ninguna funcionalidad (historial de pedidos, carrito guardado, datos personales).
- **Maneja datos sensibles.** Credenciales, y número de celular son datos críticos que deben validarse rigurosamente.
- **Tiene múltiples validaciones.** Formato de email, longitud de contraseña, unicidad de correo, formato de celular — cada una representa un caso de prueba distinto.
- **Alto impacto en el negocio.** Un fallo en el login o registro puede impedir que un cliente realice una compra, lo que representa una pérdida directa para Falabella.

### Criterios de aceptación identificados

#### Formulario de Login
| Campo | Validación identificada |
|---|---|
| Email | Debe tener formato válido (contener @ y dominio) |
| Email | Debe estar registrado en el sistema |
| Contraseña | No puede estar vacía |
| Contraseña | Debe coincidir con la registrada para ese email |
| Ambos campos | No pueden enviarse vacíos |

#### Formulario de Registro
| Campo | Validación identificada |
|---|---|
| Email | Formato válido con @ y dominio |
| Email | No debe estar previamente registrado |
| Contraseña | Mínimo 8 caracteres |



### Análisis previo al diseño de casos

**1. ¿Qué campos tiene el formulario?**

- **Login:** Email, Contraseña
- **Registro:** Nombre completo, Email, Contraseña,confirmar contraseña, rol en el sistema.

**2. ¿Qué validaciones aplica el sistema?**

- No acepta emails sin `@` ni sin dominio
- La contraseñas al momento de registrarse deben de coincidir
- No permite registrar un email ya existente
- Los campos obligatorios no pueden enviarse vacíos

**3. ¿Cuáles son los rangos válidos de cada campo?**

| Campo | Rango / Formato válido |
|---|---|
| Email | Formato: `usuario@dominio.com` |




## 4.  Matriz de casos de prueba (Excel)

> 🔗 **[Ver matriz completa en Excel →](https://docs.google.com/spreadsheets/d/1iuPTvSQnfy-sVdxpXogCz3pOEy0ifEN3iGEnoWh6Na8/edit?usp=sharing)**

La matriz contiene **8 casos de prueba** .
