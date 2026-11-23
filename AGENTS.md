# Estándares y Directrices para Agentes de IA Autónomos en Desarrollo Web

> **Estándar universal para ingeniería asistida por IA, agentes autónomos y equipos de desarrollo full-stack.**  
> Diseñado para crear aplicaciones web de alto rendimiento, seguras, humanas, accesibles y listas para producción.

> [!NOTE]
> *(To read this complete specification in English, please visit [AGENTS.md](AGENTS.md)).*

---

## 0. Protocolo Obligatorio: Entrevista Interactiva de Inicio (Onboarding)

> [!IMPORTANT]
> **REGLA FUNDAMENTAL PARA EL AGENTE DE IA:** Antes de escribir, modificar o estructurar una sola línea de código del proyecto, el agente **DEBE** iniciar una entrevista interactiva con el usuario. El agente recopilará las respuestas a las siguientes 5 dimensiones para adaptar la arquitectura, el estilo visual, los textos y el marco legal:

### 1. Identidad de Marca y Contexto Visual
- **Nombre de la Empresa y Misión:** ¿Cómo se llama el negocio, qué hace y qué valor aporta a sus clientes?
- **Logotipo y Recursos Visuales:** ¿Cuáles son los colores predominantes, formas y personalidad del logo? El agente debe extraer los tokens de color (Primario, Acento, Fondo, Superficie) y sugerir combinaciones tipográficas armonizadas con este ancla visual.
- **Tono y Personalidad de Marca:** Lujo, clínico/dermatológico, minimalista, orgánico/botánico, técnico/desarrollador, fresco/divertido o institucional.

### 2. Productos, Servicios y Modelo de Negocio
- **Oferta Comercial:** Productos físicos (e-commerce), descargas digitales, suscripciones SaaS, consultorías/citas o captura de clientes potenciales (leads).
- **Oferta Estrella:** ¿Cuál es el producto principal o el objetivo central de conversión?

### 3. Casos de Uso y Requisitos del Sistema
- **Requisitos Funcionales:** Capacidades exactas del usuario (navegación de catálogo, bolsa de compras en tiempo real, checkout multi-paso, agendamiento de citas, test de diagnóstico interactivo, pedidos directos a WhatsApp, calificaciones y comentarios por estrellas, motor de cupones de descuento).
- **Requisitos No Funcionales:** Metas de rendimiento (Core Web Vitals: LCP < 2.5s, CLS < 0.1, INP < 200ms), estándar de accesibilidad (WCAG 2.1 Nivel AA), diseño móvil prioritario (*mobile-first*) y cero saltos de diseño (*layout shift*).

### 4. Elección de Infraestructura, Servidor y Base de Datos
El usuario tiene total libertad para elegir cualquier proveedor de nube o base de datos. El agente debe consultar qué stack prefiere y ofrecer la recomendación de referencia de este estándar:
- **Hosting en el Borde y DNS Recomendado:** **Cloudflare Pages & Workers** (CDN global instantánea, ejecución serverless en el borde con ultra baja latencia, seguridad nativa y cero arranques en frío).
- **Base de Datos y Autenticación Recomendada:** **Supabase (PostgreSQL)** (Row-Level Security estricto para aislamiento multi-inquilino, transacciones relacionales ACID, sesiones seguras en cookies HttpOnly y almacenamiento cifrado).
- *Flexibilidad Abierta:* Si el usuario prefiere AWS, Vercel, Firebase, Docker, MySQL, SQLite o MongoDB, el agente debe adaptar la arquitectura limpiamente sin romper la separación de responsabilidades.

### 5. Jurisdicción Legal y Cumplimiento Normativo
- **Jurisdicción de Operación:** ¿En qué país o marco legal opera la aplicación? (ej: Colombia: Ley 1581 / SIC, Unión Europea: RGPD, Estados Unidos: CCPA / FTC, México: LFPDPPP).
- **Contenido Legal Obligatorio:** Redactar a medida las páginas obligatorias: `/terminos`, `/privacidad`, `/cookies` y canal de atención de peticiones, quejas y reclamos (PQRS / Soporte).
- **Trazabilidad Auditable de Consentimiento:** Guardar IP del cliente, marca de tiempo UTC del servidor, versión de las políticas aceptadas y consentimiento booleano explícito.

---

## 1. Principios Fundamentales y Arquitectura

### Arquitectura Limpia y Separación de Responsabilidades
- **Separación Explícita de Archivos:** Mantén cada lenguaje en archivos dedicados (`.html`, `.css`, `.js`, `.ts`). Evita estilos en línea, scripts incrustados en atributos o archivos monolíticos desordenados.
- **Elección por Ajuste Real:** Prioriza soluciones ligeras y probadas que maximicen el rendimiento, claridad y mantenimiento sobre capas innecesarias de librerías.
- **Acceso Sin Fricción (Cero Barreras Artificiales):** Nunca ocultes ni bloquees el catálogo, precios, bolsa de compras o flujo de checkout detrás de inicios de sesión obligatorios. Permite que el visitante explore, añada al carrito y compre con total fluidez.

### Redacción Humana y Directa (Estándar Anti-Texto de IA)
- **Cero Redundancias de IA:** Prohibido el texto inflado, introducciones robóticas, descripciones obvias y adjetivos artificiales (ej: *"en el bullicioso mundo digital de hoy", "solución revolucionaria e integral"*).
- **Directo, Conciso y Humano:** Títulos cortos, descripciones prácticas y botones con etiquetas claras y naturales (ej: *"Añadir"*, *"Pedir por WhatsApp"*, *"Confirmar Pedido"*).

### Interactividad Directa en la Página (In-Place)
- Prefiere interacciones directas en la misma página (formularios limpios, acordeones fluidos, selectores de estrellas directos) sobre ventanas modales invasivas o menús desplegables pesados.

---

## 2. Pila Tecnológica Recomendada

| Capa | Tecnología Recomendada | Propósito |
| :--- | :--- | :--- |
| **Estilos y Sistema de Diseño** | Tailwind CSS / Variables CSS | Estilos escalables basados en tokens y diseño responsivo rápido |
| **Componentes de Interfaz** | Headless UI Accesible / WAI-ARIA | Primitivas de interfaz sin estilos obligados, modulares y accesibles |
| **Animación y Dinamismo** | GSAP (GreenSock) y Motion (Framer) | Líneas de tiempo interactivas de alta precisión y gestos táctiles fluidos |
| **Carruseles y Medios** | Swiper.js | Carruseles acelerados por hardware con soporte táctil prioritario |
| **Iconografía y Tipografía** | Lucide Icons (SVG) y Tipografías de alto contraste | Iconos profesionales y limpios (cero emojis informales en la interfaz) |
| **Hosting en el Borde y DNS** | Cloudflare Pages / Workers / Edge Rules | Computación en el borde global con mínima latencia y máxima seguridad |
| **Persistencia y Autenticación** | Supabase (PostgreSQL + RLS) / SQLite Edge | Integridad relacional con seguridad a nivel de fila y sesiones firmadas |

---

## 3. Metodología Estricta en 7 Pasos de Desarrollo

```mermaid
flowchart TD
    A["0. Entrevista, Descubrimiento y Marca"] --> B["1. Alcance y Requisitos Legales"]
    B --> C["2. Flujos, Estructura Base y Rutas"]
    C --> D["3. Sistema de Diseño y Estilos Dinámicos"]
    D --> E["4. Estados Frontend y UX Sin Fricción"]
    E --> F["5. Animaciones Fluidas y Microinteracciones"]
    F --> G["6. Backend, RLS y Trazabilidad"]
    G --> H["7. Auditoría, WCAG 2.1 AA y Lanzamiento"]
```

### Paso 1: Alcance, Casos de Uso y Cumplimiento Legal
- Definir las rutas exactas del usuario y los límites transaccionales.
- Responder las 3 preguntas legales obligatorias:
  1. *¿Qué datos personales específicos se recopilan y con qué finalidad?*
  2. *¿Bajo qué jurisdicción legal opera la transacción?*
  3. *¿Qué garantías, políticas de devolución y compromisos comerciales se ofrecen?*

### Paso 2: Contenido, Flujos de Conversión y Rutas Obligatorias
- Construir embudos completos y ciclos de vida del usuario.
- Incluir obligatoriamente las páginas legales estatutarias:
  - `/terminos` (Términos y Condiciones)
  - `/privacidad` (Política de Privacidad)
  - `/cookies` (Política de Cookies y Banner de Consentimiento)
  - Canal de atención directa al cliente (PQRS / Soporte)

### Paso 3: Sistema de Diseño y Jerarquía Visual
- Paleta sobria anclada al logotipo: lienzo neutro, bordes sutiles y un único color de acento intencional.
- Combinación tipográfica legible y de alto contraste (fuente display para títulos + sans-serif para lectura).
- Escala de espaciados unificada e iconografía Lucide en formato SVG (nunca emojis en componentes de producción).

### Paso 4: Frontend Robusto y Manejo de Estados
- Cubrir explícitamente los 4 estados fundamentales de cada componente:
  - **Carga (Loading):** Esqueletos elegantes con efecto shimmer o pulso sutil.
  - **Vacío (Empty):** Explicación humana y llamada a la acción clara.
  - **Error (Error):** Mensaje comprensible con opción de reintento directo.
  - **Éxito (Success):** Confirmación limpia, recibo de pedido o retroalimentación inmediata.
- Todo formulario que recolecte datos personales debe incluir **dos casillas independientes de consentimiento, desmarcadas por defecto**:
  - `[ ] He leído y acepto los Términos y Condiciones`
  - `[ ] He leído y acepto la Política de Privacidad`

### Paso 5: Motor de Animación y Rendimiento
- Animar únicamente propiedades compuestas por GPU: `transform` y `opacity`.
- Emplear GSAP ScrollTrigger o Framer Motion para entradas escalonadas y revelaciones al hacer scroll.
- Mantener las microinteracciones por debajo de `300ms` con curvas de aceleración naturales.
- Respetar siempre las preferencias de accesibilidad del usuario mediante `prefers-reduced-motion`.

### Paso 6: Seguridad de Backend y Trazabilidad Auditable
Aplicar las **20 Reglas Estrictas de Seguridad**:
1. **Row-Level Security (RLS):** Aislamiento estricto de datos en cada tabla de la base de datos.
2. **Cero Fuga de Secretos:** Jamás exponer claves de servicio (*Service Keys*), tokens privados ni credenciales en código cliente.
3. **Cookies HttpOnly y SameSite:** Almacenamiento seguro de tokens con protección activa contra CSRF.
4. **Límite de Tasa por IP (*Rate Limiting*):** Ventana deslizante para mitigar spam y ataques de fuerza bruta en endpoints públicos y mutaciones.
5. **Protección Anti-IDOR:** Autenticar y autorizar cada lectura y escritura contra la pertenencia real del usuario.
6. **Validación de Esquema y Sanitización:** Validar entradas con esquemas tipados (como Zod) tanto en cliente como en el borde.
7. **Consultas Parametrizadas:** Prevenir inyecciones SQL evitando concatenaciones de texto sin sanitizar.
8. **Almacenamiento Criptográfico de Contraseñas:** Algoritmos robustos (Argon2, bcrypt, PBKDF2) con sal única por usuario.
9. **Trazabilidad de Consentimiento:** Registrar IP, fecha/hora UTC del servidor, versión de políticas y aceptación explícita para auditorías legales.
10. **Principio de Menor Privilegio:** Limitar las claves de API únicamente a las tablas y acciones indispensables.

### Paso 7: Control de Calidad, Accesibilidad y Despliegue
- Métricas Core Web Vitals: LCP < 2.5s, FID/INP < 200ms, CLS < 0.1.
- Accesibilidad: Cumplimiento de WCAG 2.1 Nivel AA (contraste de color ≥ 4.5:1, control de foco por teclado, etiquetas ARIA).
- SEO y Rastreadores: Generación limpia de `sitemap.xml`, `robots.txt` y metadatos Open Graph.
- Analítica externa (GA4, píxeles de seguimiento): Bloqueada hasta que el usuario otorgue consentimiento explícito de cookies.

---

## 4. Flujo de Trabajo Estándar (Local Primero -> Nube)

1. **Verificación Local Obligatoria:** Todos los cambios, pruebas de integración y comprobaciones de seguridad deben correr y pasar localmente primero.
2. **Despliegue Automatizado a Cloudflare Pages:**
   ```bash
   # Configurar credencial de cuenta Cloudflare
   export CLOUDFLARE_ACCOUNT_ID="tu_cloudflare_account_id"

   # Desplegar aplicación o tienda a producción
   npx wrangler pages deploy ./dist --project-name "mi-proyecto-web" --branch main
   ```
3. **Validación en Vivo:** Comprobar inmediatamente la URL pública desplegada antes de dar por completado el trabajo.

---

## 5. Créditos y Agradecimientos al Ecosistema Abierto

Este estándar sintetiza las mejores prácticas de la comunidad global de código abierto:
- [Tailwind CSS](https://tailwindcss.com) por Tailwind Labs
- [Lucide Icons](https://lucide.dev) por el Proyecto y Comunidad Lucide
- [GSAP](https://gsap.com) por GreenSock
- [Swiper](https://swiperjs.com) por Vladimir Kharlampidi
- [Cloudflare Pages & Workers](https://developers.cloudflare.com/pages/) por Cloudflare
- [Supabase](https://supabase.com) por el Equipo Supabase y la Comunidad PostgreSQL
- [Iniciativa de Accesibilidad Web W3C (WAI-ARIA)](https://www.w3.org/WAI/)

---

## Licencia

Este framework y sus instrucciones son de código abierto bajo la [Licencia MIT](LICENSE).  
Siéntete libre de usarlo, compartirlo y adaptarlo para tus propios agentes de IA, repositorios y proyectos.
