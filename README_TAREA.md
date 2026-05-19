# Casos de Prueba — Saga Falabella Perú

---

## 1. Portada

| Campo | Detalle |
|---|---|
| **Nombre completo** | *VILA CAYO, NAYHERLY DIANETH* |
| **Código universitario** | *27202120* |
| **Curso** | S489 — Pruebas y Aseguramiento de Calidad de Software |
| **Docente** | Ing. Lizbeth Jaico |
| **Sistema elegido** | Saga Falabella Perú — E-commerce |
| **URL del sistema** | https://www.falabella.com.pe |
| **Módulo analizado** | Login / Registro |
| **Universidad** | Universidad Nacional de San Cristóbal de Huamanga |
| **Fecha** | Mayo 2026 |

---

## 2. Descripción del sistema bajo prueba

Saga Falabella Perú es una de las principales tiendas por departamento del país, con presencia física en varias ciudades y una plataforma de comercio electrónico disponible en [https://www.falabella.com.pe](https://www.falabella.com.pe).

Su tienda online permite a millones de clientes peruanos explorar y comprar productos de moda, tecnología, hogar, deportes y más, desde cualquier dispositivo con conexión a internet. El sistema web ofrece funcionalidades como autenticación segura de usuarios, registro de nuevas cuentas con validación de datos personales, gestión del carrito de compras, seguimiento de pedidos, administración de direcciones de envío y procesamiento de pagos.

Cuenta con validaciones en todos sus formularios, proporcionando una experiencia de compra segura, rápida y accesible desde cualquier navegador moderno.

---

## 3.  Módulo elegido y justificación

### Módulo: Login y Registro

Módulos: Login, Registro, Búsqueda y Carrito de Compras


- **Son funcionalidades críticas del flujo de compra.** El usuario necesita registrarse o iniciar sesión para acceder a funcionalidades personalizadas, buscar productos y agregarlos al carrito antes de concretar una compra.
- **Representan la experiencia principal del cliente en el sistema.** La búsqueda permite encontrar productos rápidamente, mientras que el carrito gestiona los artículos seleccionados para la compra. Un fallo en cualquiera de estos módulos afecta directamente la experiencia del usuario.
- **Manejan información sensible y procesos importantes.** Los módulos de Login y Registro procesan datos personales como credenciales, DNI y número de celular, los cuales requieren validaciones rigurosas para garantizar seguridad y privacidad.
- **Poseen múltiples validaciones funcionales y de negocio.** Se validan formatos de correo electrónico, longitud y seguridad de contraseñas, unicidad de usuarios, disponibilidad de productos, actualización del carrito, cantidad de productos y resultados de búsqueda relacionados. Cada validación representa distintos casos de prueba funcionales y de borde.

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
| Celular | Solo dígitos, exactamente 8 caracteres (formato peruano) |
| DNI | Solo dígitos, formato válido |

#### Formulario de Búsqueda
| Campo | Validación identificada |
|---|---|
| Barra de búsqueda | Permite texto alfanumérico |
| Término de búsqueda | Campo obligatorio |

#### Formulario de Carrito
| Carrito vacío | Mostrar mensaje "tu carrito esta vacío"|
| Botón agregar al carrito | Debe agregar correctamente el producto|

### Análisis previo al diseño de casos

**1. ¿Qué campos tiene el formulario?**

- **Login:** Email, Contraseña
- **Registro:** Nombre, Apellido , Email, Contraseña, Tipo de documento, N° de documento, Celular
- **Búsqueda**: Permite buscar los productos.
- **Carrito**: Permite añadir productos añ carrito

**2. ¿Qué validaciones aplica el sistema?**

- No acepta emails sin `@` ni sin dominio
- La contraseña tiene un mínimo de 8 caracteres
- No permite registrar un email ya existente
- El celular solo acepta dígitos con formato peruano (9 dígitos, empieza con 9)
- Los campos obligatorios no pueden enviarse vacíos

**3. ¿Cuáles son los rangos válidos de cada campo?**

| Campo | Rango / Formato válido |
|---|---|
| Email | Formato: `usuario@dominio.com` |
| Contraseña | Mínimo: **8 caracteres** (N), Inválido: **7 o menos** (N-1) |
| Celular | 9 dígitos, debe iniciar con 9 |
| DNI | 8 dígitos numéricos |


## 4.  Matriz de casos de prueba (Excel)

> 🔗 **[Ver matriz completa en Excel →](https://docs.google.com/spreadsheets/d/15C6u4wKZsb--4JO8DFmBxKe3wvjgUyyUP8AlhEE5vXI/edit?usp=sharing)**

La matriz contiene **10 casos de prueba** .

