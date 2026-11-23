# Framework de Desarrollo Web para Agentes de IA Autónomos (AGENTS)

> **El estándar universal en español para ingeniería asistida por IA, agentes autónomos y desarrollo web moderno.**

[![Licencia: MIT](https://img.shields.io/badge/Licencia-MIT-blue.svg)](LICENSE)
[![Estándar: AGENTS](https://img.shields.io/badge/Est%C3%A1ndar-AGENTS.md-emerald.svg)](AGENTS.md)

Este repositorio contiene la especificación completa y las directrices para configurar asistentes de código con IA (Antigravity, Cursor, Windsurf, Copilot, Cline, etc.), asegurando que construyan aplicaciones web de alta gama, rápidas, accesibles, seguras y libres de los errores y textos inflados típicos de la IA.

---

## 🌟 Puntos Clave del Estándar

1. **Protocolo Obligatorio de Entrevista Inicial (Fase 0):**  
   Antes de generar código, el agente de IA realiza una entrevista interactiva para conocer:
   - Identidad, misión y público objetivo de la empresa.
   - **Análisis del logo:** Extrae los colores predominantes para generar la paleta CSS/Tailwind y la tipografía adecuada.
   - Requisitos funcionales y no funcionales.
   - Elección abierta de servidor y base de datos (con la recomendación oficial: **Cloudflare Pages/Workers** + **Supabase PostgreSQL**).
   - Adaptación legal según el país de operación (`/terminos`, `/privacidad`, `/cookies` y PQRS).

2. **Redacción Humana y Directa (Anti-Texto de IA):**  
   Prohíbe estrictamente frases largas, párrafos obvios, redundancias y adjetivos artificiales. Exige lenguaje claro, conciso y orientado a la acción.

3. **Acceso Sin Fricción (Zero-Friction):**  
   Garantiza que el catálogo, precios, carrito y checkout nunca se oculten ni se bloqueen exigiendo inicio de sesión obligatorio.

4. **Interactividad Directa en la Página:**  
   Prioriza formularios y acciones directas en la interfaz frente a ventanas emergentes o modales invasivos.

5. **20 Reglas de Seguridad OWASP:**  
   Aislamiento con Row-Level Security (RLS), sesiones seguras en cookies HttpOnly, control de límites por IP (*rate limiting*), protección anti-IDOR y consentimiento legal auditable.

6. **Metodología Estricta en 7 Pasos:**  
   Desde el descubrimiento de marca hasta la auditoría de Core Web Vitals (LCP < 2.5s, CLS < 0.1, INP < 200ms) y accesibilidad WCAG 2.1 AA.

---

## 📁 Estructura del Repositorio

```
.
├── AGENTS.md    # Estándar con las instrucciones completas para tu agente de IA
├── README.md    # Presentación y documentación en español
└── LICENSE      # Licencia de código abierto MIT
```

---

## 🚀 Cómo Usarlo en tu Proyecto

### Opción A: En cualquier Asistente o Agente de IA
1. Clona o descarga este repositorio.
2. Copia el archivo `AGENTS.md` en la raíz de tu proyecto web:
   ```bash
   cp AGENTS.md /ruta/a/tu/proyecto/
   ```
3. Al iniciar conversación con tu IA, indícale:  
   *"Sigue al pie de la letra las reglas, protocolos y pasos especificados en `AGENTS.md`."*

### Opción B: Descargar el archivo ZIP
Puedes descargar directamente el paquete comprimido `.zip` para usarlo sin necesidad de usar la terminal.

---

## 🛠️ Pila Tecnológica Recomendada

| Capa | Tecnología | Por qué se recomienda |
| :--- | :--- | :--- |
| **Estilos** | Tailwind CSS / Variables CSS | Diseño basado en tokens, ultrarrápido y sin sobrepeso |
| **Componentes** | Headless UI Accesible / WAI-ARIA | Primitivas accesibles con control total de navegación |
| **Animación** | GSAP y Motion (Framer) | Microinteracciones fluidas por hardware bajo 300ms |
| **Carruseles** | Swiper.js | Soporte táctil móvil prioritario y acelerado por GPU |
| **Iconos** | Lucide Icons (SVG) | Iconografía sobria y profesional (cero emojis en UI) |
| **Hosting en el Borde** | Cloudflare Pages & Workers | Red global con latencia mínima y cero arranques en frío |
| **Base de Datos y Auth** | Supabase (PostgreSQL + RLS) | Seguridad estricta por fila, sesiones firmadas y ACID |

---

## 🤝 Créditos y Agradecimientos

Este estándar reúne y sintetiza las mejores herramientas de la comunidad de código abierto:
- [Tailwind CSS](https://tailwindcss.com) por Tailwind Labs
- [Lucide Icons](https://lucide.dev) por el Proyecto y Comunidad Lucide
- [GSAP](https://gsap.com) por GreenSock
- [Swiper](https://swiperjs.com) por Vladimir Kharlampidi
- [Cloudflare Pages & Workers](https://developers.cloudflare.com/pages/) por Cloudflare
- [Supabase](https://supabase.com) por Supabase y la comunidad PostgreSQL
- [W3C Web Accessibility Initiative (WAI-ARIA)](https://www.w3.org/WAI/)

---

## 📄 Licencia

Publicado bajo la [Licencia MIT](LICENSE). Totalmente libre y gratuito para desarrolladores, agencias y creadores de agentes de IA en todo el mundo.
