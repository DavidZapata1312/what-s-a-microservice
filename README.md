# 🧩 Microservicios

## ¿Qué es un microservicio?

Un **microservicio** es una **unidad independiente y autónoma de software** diseñada para ejecutar una función específica dentro de un sistema más grande.  
A diferencia de una aplicación monolítica (donde todo el código está en un solo bloque), los microservicios permiten dividir la aplicación en **pequeños módulos especializados** que se comunican entre sí mediante **APIs o mensajería**.

Cada microservicio tiene su **propia lógica de negocio, base de datos y ciclo de vida**, lo que permite que pueda desarrollarse, desplegarse y escalarse de forma individual sin afectar a los demás.

---

## 🧠 Diferencia entre un servicio de NestJS y un microservicio

En **NestJS**, un **servicio (`@Injectable()`)** es una clase reutilizable que contiene la lógica de negocio dentro de **una misma aplicación Nest**.  
Estos servicios **no son independientes**, sino que dependen del contexto global del proyecto donde están definidos.

En cambio, un **microservicio**:
- Es una **aplicación separada** (puede vivir en otro servidor o contenedor).  
- Se comunica con otros microservicios o servicios principales por **mensajes o HTTP**.  
- Tiene **su propio entorno, dependencias y base de datos**.  
- Puede ser desarrollado incluso en **otro lenguaje o framework**, siempre que siga el protocolo de comunicación definido.  

> 💡 En resumen:
> - **Servicio de NestJS:** parte interna del mismo sistema.  
> - **Microservicio:** sistema autónomo que colabora con otros mediante la red.

---

## 💳 Ejemplo: Microservicios en pasarelas de pago

Empresas como **Mercado Libre** o **Amazon** usan microservicios para manejar sus **procesos de pago**.  
Por ejemplo, cuando haces una compra:
1. El servicio principal (pedidos) llama al microservicio de pagos.  
2. Ese microservicio valida el método de pago y contacta con los proveedores externos (Visa, PayPal, etc.).  
3. Devuelve la confirmación sin que el resto del sistema quede bloqueado.

Así, si el sistema de pagos falla, la web o app siguen operando normalmente en otras funciones.

---

## 🌐 Otros ejemplos de uso de microservicios

Las grandes plataformas tecnológicas han adoptado arquitecturas de microservicios por su **flexibilidad, resiliencia y escalabilidad**.  
Aquí algunos casos comunes:

### 🔵 Meta (Facebook, Instagram)
Meta usa cientos de microservicios que manejan desde:
- **Autenticación y seguridad de sesión** (gestión de tokens, inicios de sesión simultáneos).  
- **Feed personalizado:** un microservicio analiza tus interacciones para decidir qué publicaciones mostrarte.  
- **Mensajería y notificaciones:** otro microservicio maneja las notificaciones push y los mensajes en tiempo real (por ejemplo, Messenger).  
Cada una de estas partes puede actualizarse sin detener toda la red social.

---

### 🔴 YouTube (Google)
YouTube también está construido sobre una arquitectura distribuida con microservicios como:
- 🎞️ **Procesamiento de videos:** un microservicio convierte los videos a múltiples calidades (240p, 480p, 1080p, etc.).  
- 💬 **Comentarios:** otro se encarga exclusivamente de almacenar y servir comentarios.  
- 🔔 **Recomendaciones:** uno de los más complejos, dedicado a sugerirte contenido usando IA.  
- 💰 **Monetización y anuncios:** un servicio distinto maneja la inserción y control de publicidad en cada país.  

Esto permite que YouTube siga funcionando incluso si un servicio puntual (como el de comentarios) presenta fallas temporales.

---

### 🟣 Netflix
Netflix fue uno de los pioneros en el uso masivo de microservicios. Su sistema está dividido en cientos de ellos:
- **Usuarios y perfiles**  
- **Recomendaciones personalizadas**  
- **Streaming y codificación de video**  
- **Control de ancho de banda por región**

Cada uno es independiente, y se comunican mediante APIs internas y colas de mensajería.

---

## 🚀 Importancia actual en el mercado

Los microservicios son hoy **la base de las arquitecturas escalables y resilientes** en empresas modernas.  
Permiten que diferentes equipos trabajen sobre módulos independientes, sin depender del ciclo de despliegue de toda la aplicación.

### Ventajas principales:
- ⚙️ **Escalabilidad:** cada componente puede crecer de forma independiente según su demanda.  
- 🧱 **Modularidad:** separación clara de responsabilidades.  
- 🔄 **Despliegue continuo:** se pueden actualizar partes del sistema sin interrumpir el servicio.  
- 🌍 **Diversidad tecnológica:** permiten mezclar lenguajes, frameworks y bases de datos según el caso.  
- 🛡️ **Resiliencia:** los errores en un microservicio no afectan al resto del ecosistema.

Por eso, empresas como **Netflix, Amazon, Meta, Mercado Libre, Google o Spotify** basan sus plataformas en **microservicios desacoplados**, logrando tiempos de respuesta bajos, disponibilidad constante y una enorme capacidad de evolución.
