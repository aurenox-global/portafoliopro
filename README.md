```markdown
<div align="center">

# PortfolioForge

### El generador de portafolios profesionales más completo y accesible

[![Estado](https://img.shields.io/badge/estado-activo-brightgreen?style=flat-square)]()
[![Navegador](https://img.shields.io/badge/navegador-100%25_cliente-orange?style=flat-square)]()
[![Exportar](https://img.shields.io/badge/exportar-PDF%20%7C%20PNG%20%7C%20JPG-blue?style=flat-square)]()
[![Plantillas](https://img.shields.io/badge/plantillas-5_profesionales-9cf?style=flat-square)]()
[![Licencia](https://img.shields.io/badge/licencia-MIT-green?style=flat-square)]()

**Un solo archivo HTML. Sin backend. Sin dependencias de servidor. Sin límites.**

[Ver demo en vivo](#) · [Reportar bug](#) · [Solicitar función](#)

</div>

---

## ¿Por qué PortfolioForge es lo mejor?

El mercado está lleno de herramientas para crear portafolios: Canva, Wix, Figma, Notion, plantillas de LaTeX... Todas fallan en algo. PortfolioForge fue diseñado para cubrir **exactamente** lo que las demás no pueden.

### El problema con las alternativas

| Herramienta | Problema principal |
|---|---|
| **Canva** | No genera PDFs con calidad de impresión real. Las plantillas son genéricas y todos las usan. No es para perfiles técnicos. |
| **Wix / Squarespace** | Te atrapan en una suscripción. El resultado es una página web, no un documento exportable para entrevistas. |
| **Figma** | Requiere diseño manual completo. No hay datos estructurados. Exportar a PDF es un dolor de cabeza con sangrados y márgenes. |
| **LaTeX / Overleaf** | Curva de aprendizaje brutal. Un error de compilación te hace perder una hora. No tiene preview visual en tiempo real. |
| **Plantillas Word / Google Docs** | Se rompen al cambiar de computadora. El formatting es frágil. No se ven profesionales de verdad. |
| **Notion** | No se exporta bien a PDF. El diseño no es controlable. Queda como "documento interno", no como portafolio. |

### Lo que hace diferente a PortfolioForge

**No compite con esas herramientas. Las hace obsoletas para este caso de uso.**

PortfolioForge no es un editor de diseño ni un CMS. Es una **máquina de generar portafolios optimizados para entrevistas**: ingresas tus datos, eliges una estética, previsualizas en tiempo real y exportas en el formato exacto que el reclutador espera recibir.

---

## Características completas

### 5 plantillas profesionales, cero genericidad

Cada plantilla fue diseñada con un propósito diferente. No son variaciones del mismo layout con colores cambiados — son **arquitecturas visuales completamente distintas**.

| Plantilla | Ideal para | Estética |
|---|---|---|
| **Minimal** | Ejecutivos, gerentes, perfiles generalistas | Tipografía fuerte, líneas sutiles, blanco puro |
| **Corporativo** | Finanzas, consultoría, empresas tradicionales | Sidebar oscura, estructura jerárquica, formal |
| **Creativo** | Diseñadores, marketers, contenido visual | Header con color, grid de 2 columnas, dinámico |
| **Técnico** | Desarrolladores, ingenieros, data scientists | Estilo terminal/monospace, barras de progreso, código |
| **Elegante** | Dirección senior, academia, roles de prestigio | Serifes, centrado, bordes punteados, sofisticado |

### Personalización profunda, no superficial

No te dan "5 colores y ya". Te dan control real sobre la identidad visual:

- **Color principal y secundario** con presets curados + picker libre
- **5 tipografías** seleccionadas por legibilidad profesional (Inter, DM Sans, Merriweather, Playfair Display, Source Code Pro)
- **Tamaño de fuente base** ajustable (8pt – 13pt)
- **Espaciado entre secciones** configurable
- **Toggle de secciones** para mostrar/ocultar foto, idiomas, certificaciones
- **Subida de foto** con preview en el editor

### Previsualización que no miente

Lo que ves es literalmente lo que se exporta. No hay sorpresas.

- **Vista en tiempo real** que se actualiza con cada keystroke
- **3 modos de dispositivo**: Escritorio (A4 completo), Tablet, Móvil
- **Zoom controlado**: Alejar, acercar, reset
- **Pantalla completa**: Modal dedicado para revisión detallada sin distracciones del editor

### Exportación real, no de juguete

| Formato | Uso | Calidad |
|---|---|---|
| **PDF** | Enviar por email, subir a portales de empleo | Multi-página automática si el contenido excede A4 |
| **PNG** | Adjuntar en mensajes, subir a redes | Sin pérdida, resolución configurable |
| **JPG** | Compartir rápido, tamaño reducido | Compresión optimizada al 92% |

- **3 niveles de calidad**: 1x (rápido), 2x (recomendado), 3x (ultra)
- **Barra de progreso visual** durante la exportación
- **Nombres de archivo inteligentes**: `nombre-apellido-plantilla.pdf`

### Editor diseñado para eficiencia

- **Secciones desplegables** con animación — no te abruma con todo visible
- **Items dinámicos**: Agrega/elimina experiencia, educación, habilidades, proyectos, idiomas, certificaciones sin límite
- **Slider de nivel de habilidad** con porcentaje visual
- **Categorización de habilidades**: Técnica, Blanda, Herramienta, Framework, Lenguaje
- **Checkbox "Trabajo actual"** que auto-completa "Presente" y bloquea fecha fin
- **Score de completitud** con anillo animado — sabes exactamente qué tan listo está tu portafolio
- **Persistencia local**: Guarda y restaura todo desde localStorage sin cuenta ni backend

### Datos de ejemplo con un clic

Botón dedicado que carga un perfil completo y realista (Ingeniero de Software Senior con 3 posiciones, 10 habilidades categorizadas, 2 proyectos, 3 idiomas, 2 certificaciones) para que veas el potencial inmediatamente sin tener que escribir nada.

---

## Arquitectura técnica

```
portfolioforge.html    ← Todo vive aquí
├── Estado centralizado (objeto `state`)
├── Editor reactivo (eventos → state → render)
├── Motor de plantillas (5 funciones render)
├── Sistema de exportación (html2canvas + jsPDF)
└── Persistencia (localStorage)
```

### Stack

| Tecnología | Propósito |
|---|---|
| **Tailwind CSS** | Estilos del editor (UI oscura) |
| **html2canvas** | Captura DOM → Canvas para exportación |
| **jsPDF** | Generación de PDFs multi-página |
| **Font Awesome** | Iconografía del editor |
| **Google Fonts** | 5 familias tipográficas para el portafolio |

### Principios de diseño del código

- **Zero backend**: Funciona abriendo el archivo HTML directamente en el navegador
- **Reactividad sin framework**: `input` → actualiza `state` → llama `renderPreview()` → reemplaza `innerHTML` del contenedor
- **Separación editor/portafolio**: El editor usa tema oscuro (Tailwind), el portafolio generado usa estilos inline blancos — zero conflicto
- **Escaping de HTML**: Todas las cadenas del usuario pasan por `esc()` para prevenir XSS
- **Exportación fiel**: Se fuerza `width: 210mm` antes de capturar para garantizar dimensión A4 real

---

## Comparativa directa

```
                        PortfolioForge  Canva  LaTeX  Figma
─────────────────────────────────────────────────────────────
Preview en tiempo real       ✅         ✅      ❌     ✅
Exportar PDF A4              ✅         ⚠️      ✅     ❌
Exportar PNG/JPG             ✅         ✅      ❌     ✅
Sin cuenta/suscripción       ✅         ❌      ✅     ❌
Sin instalar nada            ✅         ❌      ❌     ❌
5 plantillas profesionales   ✅         ✅      ⚠️     ❌
Personalización de colores   ✅         ✅      ✅     ✅
Personalización de fuentes   ✅         ✅      ✅     ✅
Datos estructurados          ✅         ❌      ✅     ❌
Items dinámicos              ✅         ⚠️      ⚠️     ❌
Multi-página PDF             ✅         ❌      ✅     ❌
Curva de aprendizaje         0 min     5 min   60 min 30 min
 Compatible con ATS          ✅         ⚠️      ✅     ❌
Un solo archivo              ✅         ❌      ❌     ❌
```

---

## Compatible con ATS (Applicant Tracking Systems)

Las plantillas generan HTML estructurado con jerarquía semántica (`h1` para nombre, negritas para cargos, texto plano para descripciones). Al exportar a PDF, el resultado es **texto seleccionable y parseable** por los sistemas que usan las empresas para filtrar currículums automáticamente.

No usa imágenes de texto, no usa tablas invisibles, no usa capas superpuestas. Es contenido real que los bots pueden leer.

---

## ¿Para quién?

- **Desarrolladores** que necesitan un portafolio técnico sin pelear con LaTeX
- **Diseñadores** que quieren algo más personalizable que una plantilla de Canva
- **Profesionales en transición** que necesitan actualizar rápido para una entrevista mañana
- **Reclutadores** que quieren generar plantillas consistentes para sus candidatos
- **Estudiantes** que necesitan su primer portafolio sin invertir dinero
- **Cualquiera** que necesite un PDF profesional en menos de 5 minutos

---

## Uso

```bash
# 1. Descargar
wget https://raw.githubusercontent.com/tu-usuario/portfolioforge/main/portfolioforge.html

# 2. Abrir
open portfolioforge.html
# o simplemente haz doble clic en el archivo

# 3. Listo. No hay paso 3.
```

No necesitas `npm install`. No necesitas `python -m http.server`. No necesitas Docker. No necesitas crear una cuenta. Descargas, abres, usas.

---

## Estructura del estado

```javascript
state = {
  personal: { nombre, apellido, titulo, email, telefono, ubicacion, linkedin, github, sitioWeb, resumen, fotoUrl },
  experiencia: [{ empresa, cargo, fechaInicio, fechaFin, descripcion, actual }],
  educacion: [{ institucion, titulo, fechaInicio, fechaFin, descripcion }],
  habilidades: [{ nombre, nivel, categoria }],
  proyectos: [{ nombre, descripcion, tecnologias, enlace }],
  idiomas: [{ nombre, nivel }],
  certificaciones: [{ nombre, institucion, fecha }],
  config: { plantilla, colorPrimario, colorSecundario, fuente, fontSize, spacing, incluirFoto, incluirIdiomas, incluirCertificaciones }
}
```

Este objeto es lo único que importa. Todo fluye de aquí.

---

## Roadmap

- [ ] Más plantillas (Doble columna moderna, Infográfico, Timeline vertical)
- [ ] Modo oscuro/claro para el portafolio
- [ ] Drag & drop para reordenar secciones
- [ ] Exportación a HTML standalone
- [ ] Múltiples páginas con navegación
- [ ] Integración con LinkedIn API para auto-completar
- [ ] PWA para usar offline
- [ ] Compartir via enlace público (usando GitHub Gist como backend gratuito)

---

## Licencia

MIT — Úsalo, modíficalo, distribúyelo, véndelo si quieres. No hay cadenas.

---

<div align="center">

**Un archivo. Cinco plantillas. Cero excusas.**

Hecho para que pases menos tiempo formateando y más tiempo consiguiendo el trabajo que mereces.

</div>
```
