# Contexto del Proyecto: Asesoría Financiera Terán

## Información General

**Nombre del proyecto:** Asesoría Financiera Terán
**Tecnología:** Astro 5.16.11
**Tipo:** Sitio web de servicios financieros
**Estado:** En desarrollo activo

---

## Información del Negocio

### Datos de Contacto
- **Email:** contacto@asesoriafinancierateran.com
- **WhatsApp:** +52 55 6413 0072
- **Ubicación:** Ciudad de México (no se muestra públicamente)

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

## Estructura del Proyecto

```
src/
├── components/
│   ├── Header.astro        # Navegación con menú móvil funcional
│   └── Footer.astro        # Footer con contacto (solo email y WhatsApp)
├── layouts/
│   ├── BaseLayout.astro    # Layout principal con SEO
│   └── ServicioLayout.astro # Layout para páginas de servicios individuales
├── pages/
│   ├── index.astro         # Página de inicio
│   ├── nosotros.astro      # Página del equipo
│   ├── faqs.astro          # Preguntas frecuentes (accordion)
│   ├── contacto.astro      # Formulario con integración n8n
│   └── servicios/
│       ├── index.astro     # Índice de servicios (cards)
│       ├── seguros.astro
│       ├── inversiones.astro
│       ├── creditos.astro
│       ├── educativo.astro
│       ├── retiro.astro
│       └── juridico.astro
└── styles/
    └── global.css          # Variables CSS y estilos globales
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
- [x] **Hero Slider** con 3 slides promocionales y auto-play
- [x] **Imagen de fondo en hero** con overlay degradado
- [x] Página "Nosotros" con equipo (placeholders para fotos)
- [x] Página de servicios (índice con cards)
- [x] 6 subpáginas de servicios individuales (diseño orientado a conversión)
- [x] Página de FAQs con accordion interactivo
- [x] Página de contacto con formulario
- [x] Header con navegación, menú móvil responsive y **submenú de servicios**
- [x] Footer actualizado (solo email y WhatsApp)
- [x] Diseño responsive completo

### 🔲 Pendiente
- [ ] Integración del webhook de n8n (placeholder en contacto.astro)
- [ ] Fotos reales del equipo
- [ ] Redes sociales reales (Facebook, Instagram)
- [ ] Política de privacidad y términos de servicio
- [ ] Posible integración de analytics

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
```

---

## Archivos de Referencia del Cliente

- `Comentarios_pagina.pdf` - Textos curados por el cliente
- `Comentarios Página.pptx` - Versión original en PowerPoint

---

## Notas de Diseño

### Página de Servicios Individuales
Cada servicio tiene su propia página con:
- Hero con icono grande y CTA principal
- Secciones alternas (blanco/gris) para dinamismo
- Cards de beneficios/tipos
- CTAs intermedios para aumentar conversión
- Lista de características con checks
- CTA final prominente
- Navegación a otros servicios

### FAQs
7 preguntas frecuentes con accordion. El JavaScript permite abrir/cerrar y solo muestra una respuesta a la vez.

### Formulario de Contacto
- Validación HTML5 nativa
- Estados de loading/éxito/error
- Preparado para webhook (actualmente muestra en console.log si no hay webhook)

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

---

## Historial de Cambios

### Enero 2026
- Proyecto iniciado con estructura base de Astro
- Creadas todas las páginas principales
- Implementado diseño responsive
- Separados servicios en subpáginas individuales
- Integración n8n preparada (pendiente URL del webhook)

---

## Próximos Pasos Sugeridos

1. Obtener URL del webhook de n8n y configurar en `contacto.astro`
2. Recibir fotos del equipo y actualizar `nosotros.astro`
3. Configurar URLs reales de redes sociales
4. Crear páginas de Política de Privacidad y Términos
5. Configurar dominio y hosting
6. Implementar analytics (Google Analytics / Plausible)
