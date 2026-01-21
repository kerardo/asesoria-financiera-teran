# Contexto del Proyecto: Asesoría Financiera Terán

## Información General

**Nombre del proyecto:** Asesoría Financiera Terán
**Tecnología:** Astro 5.16.11
**Tipo:** Sitio web de servicios financieros
**Estado:** En producción
**Dominio:** https://asesoriafinancierateran.com
**Repositorio:** https://github.com/kerardo/asesoria-financiera-teran

---

## Información del Negocio

### Datos de Contacto
- **Email:** contacto@asesoriafinancierateran.com
- **WhatsApp:** +52 55 6413 0072
- **Cobertura:** Todo México (nacional)

### Equipo
| Nombre | Rol |
|--------|-----|
| Abraham Terán | Asesor financiero y seguros |
| Isaac Terán | Asesor financiero y créditos |
| Ulises Terán | Asesor jurídico |
| Valeria Bárcenas | Asesor jurídico |

**Nota:** Las fotos del equipo están pendientes. Actualmente se usan placeholders con iniciales.

### Servicios (6)
1. **Seguros** - Vida, salud, auto, hogar
2. **Inversión Inteligente** - Acciones, fondos, bonos
3. **Créditos** - Personales, auto, hipotecarios, empresariales
4. **Ahorro Educativo** - Planes para educación de hijos
5. **Planes de Retiro** - Estrategias de jubilación
6. **Asesoría Jurídica** - Derecho civil, familiar, patrimonial

---

## Hosting y Deploy

### Hostinger
- **Tipo:** Hosting Web compartido
- **FTP Host:** 195.179.239.72
- **Usuario FTP:** (configurado en GitHub Secrets)

### Deploy Automático con GitHub Actions
El sitio se despliega automáticamente a Hostinger cada vez que se hace push a la rama `main`.

**Archivo de configuración:** `.github/workflows/deploy.yml`

**Flujo de deploy:**
1. Hacer cambios en el código
2. `git add .`
3. `git commit -m "Descripción del cambio"`
4. `git push`
5. GitHub Actions construye y despliega automáticamente (~2 min)

**GitHub Secrets necesarios:**
| Secret | Descripción |
|--------|-------------|
| `FTP_HOST` | IP del servidor FTP (195.179.239.72) |
| `FTP_USERNAME` | Usuario FTP de Hostinger |
| `FTP_PASSWORD` | Contraseña FTP |

**Ver estado del deploy:** https://github.com/kerardo/asesoria-financiera-teran/actions

---

## SEO Implementado

### Optimizaciones Técnicas
- [x] **Sitemap XML** - Generado automáticamente con @astrojs/sitemap
- [x] **robots.txt** - Configurado en `/public/robots.txt`
- [x] **Open Graph tags** - Para compartir en Facebook/LinkedIn
- [x] **Twitter Cards** - Para compartir en Twitter
- [x] **Canonical URLs** - Evita contenido duplicado
- [x] **Schema.org JSON-LD** - Markup de negocio financiero
- [x] **Meta descriptions** - Optimizadas por página
- [x] **lang="es-MX"** - Idioma español México

### URLs SEO Importantes
- Sitemap: `https://asesoriafinancierateran.com/sitemap-index.xml`
- Robots: `https://asesoriafinancierateran.com/robots.txt`

### Pendiente SEO
- [ ] **Imagen OG** - Crear `/public/images/og-image.jpg` (1200x630px)
- [ ] Registrar en Google Search Console
- [ ] Registrar en Google Business Profile
- [ ] Obtener backlinks

---

## Estructura del Proyecto

```
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions para deploy a Hostinger
├── public/
│   ├── favicon.svg
│   ├── robots.txt              # SEO
│   └── images/
│       └── hero-bg.jpg
├── src/
│   ├── components/
│   │   ├── Header.astro        # Navegación con menú móvil funcional
│   │   └── Footer.astro        # Footer con contacto
│   ├── layouts/
│   │   ├── BaseLayout.astro    # Layout principal con SEO completo
│   │   └── ServicioLayout.astro # Layout para páginas de servicios
│   ├── pages/
│   │   ├── index.astro         # Página de inicio
│   │   ├── nosotros.astro      # Página del equipo
│   │   ├── faqs.astro          # Preguntas frecuentes
│   │   ├── contacto.astro      # Formulario de contacto
│   │   └── servicios/
│   │       ├── index.astro     # Índice de servicios
│   │       ├── seguros.astro
│   │       ├── inversiones.astro
│   │       ├── creditos.astro
│   │       ├── educativo.astro
│   │       ├── retiro.astro
│   │       └── juridico.astro
│   └── styles/
│       └── global.css          # Variables CSS y estilos globales
├── astro.config.mjs            # Configuración de Astro + sitemap
├── package.json
└── CONTEXTO-PROYECTO.md        # Este archivo
```

---

## Paleta de Colores

```css
--color-primary: #1e3a5f;    /* Azul marino */
--color-secondary: #2d5a87;  /* Azul */
--color-accent: #c9a227;     /* Dorado */
--color-text: #333333;
--color-text-light: #666666;
--color-bg: #ffffff;
--color-bg-alt: #f8f9fa;
```

---

## Funcionalidades Implementadas

### ✅ Completado
- [x] Página de inicio con hero slider, servicios, ventajas y CTA
- [x] Hero Slider con 3 slides promocionales y auto-play
- [x] Imagen de fondo en hero con overlay degradado
- [x] Página "Nosotros" con equipo (placeholders para fotos)
- [x] Página de servicios (índice con cards)
- [x] 6 subpáginas de servicios individuales
- [x] Página de FAQs con accordion interactivo
- [x] Página de contacto con formulario
- [x] Header con navegación, menú móvil responsive y submenú de servicios
- [x] Footer actualizado (solo email y WhatsApp)
- [x] Diseño responsive completo
- [x] Deploy automático a Hostinger via GitHub Actions
- [x] SEO técnico completo (sitemap, robots, OG, schema, etc.)

### 🔲 Pendiente
- [ ] Integración del webhook de n8n (placeholder en contacto.astro)
- [ ] Fotos reales del equipo
- [ ] Imagen OG para redes sociales (1200x630px)
- [ ] Redes sociales reales (Facebook, Instagram)
- [ ] Política de privacidad y términos de servicio
- [ ] Registro en Google Search Console
- [ ] Registro en Google Business Profile
- [ ] Integración de analytics

---

## Integración n8n (Formulario de Contacto)

El formulario en `/contacto` está preparado para enviar datos a un webhook de n8n.

**Ubicación del código:** `src/pages/contacto.astro`

**Buscar y reemplazar:**
```javascript
const WEBHOOK_URL = 'TU_WEBHOOK_N8N_AQUI';
```

**Datos que envía el formulario:**
```json
{
  "nombre": "string",
  "email": "string",
  "telefono": "string (opcional)",
  "servicio": "string (uno de los 6 servicios)",
  "mensaje": "string",
  "fecha": "ISO timestamp"
}
```

---

## Comandos Útiles

```bash
# Instalar dependencias
npm install

# Iniciar servidor de desarrollo
npm run dev

# Construir para producción
npm run build

# Previsualizar build de producción
npm run preview

# Desplegar cambios (después de commit)
git add .
git commit -m "Descripción del cambio"
git push
```

---

## Archivos de Referencia del Cliente

- `Comentarios_pagina.pdf` - Textos curados por el cliente
- `Comentarios Página.pptx` - Versión original en PowerPoint

---

## URLs del Sitio

| Ruta | Descripción |
|------|-------------|
| `/` | Inicio |
| `/nosotros` | Equipo |
| `/servicios` | Índice de servicios |
| `/servicios/seguros` | Seguros |
| `/servicios/inversiones` | Inversión Inteligente |
| `/servicios/creditos` | Créditos |
| `/servicios/educativo` | Ahorro Educativo |
| `/servicios/retiro` | Planes de Retiro |
| `/servicios/juridico` | Asesoría Jurídica |
| `/faqs` | Preguntas Frecuentes |
| `/contacto` | Formulario de Contacto |
| `/sitemap-index.xml` | Sitemap para Google |
| `/robots.txt` | Instrucciones para bots |

---

## Historial de Cambios

### 21 Enero 2026
- Configurado deploy automático a Hostinger con GitHub Actions (FTP)
- Implementado SEO técnico completo:
  - Sitemap XML automático
  - robots.txt
  - Open Graph y Twitter Cards
  - Schema.org JSON-LD para negocio financiero
  - Canonical URLs
  - Meta descriptions optimizadas
- Sitio en producción: https://asesoriafinancierateran.com

### 20 Enero 2026
- Proyecto iniciado con estructura base de Astro
- Creadas todas las páginas principales
- Implementado diseño responsive
- Separados servicios en subpáginas individuales
- Integración n8n preparada (pendiente URL del webhook)

---

## Próximos Pasos Sugeridos

1. **Crear imagen OG** - `/public/images/og-image.jpg` (1200x630px) con logo y colores de marca
2. **Registrar en Google Search Console** - Para monitorear indexación
3. **Registrar en Google Business Profile** - Para aparecer en Google Maps
4. Obtener URL del webhook de n8n y configurar en `contacto.astro`
5. Recibir fotos del equipo y actualizar `nosotros.astro`
6. Configurar URLs reales de redes sociales
7. Crear páginas de Política de Privacidad y Términos
8. Implementar analytics (Google Analytics / Plausible)

---

## Notas Técnicas

### Imagen OG (Open Graph)
La imagen OG es la vista previa que aparece cuando se comparte el sitio en redes sociales (WhatsApp, Facebook, LinkedIn, Twitter).

**Especificaciones:**
- Tamaño: 1200 x 630 píxeles
- Ubicación: `/public/images/og-image.jpg`
- Contenido sugerido: Logo + "Seguros | Inversiones | Créditos" + colores de marca

### BaseLayout.astro
Contiene toda la configuración SEO. Si necesitas modificar meta tags, Open Graph, o Schema markup, edita este archivo.
