# Lineamientos Visuales HMG — Estándar para Guías Gráficas y Landings

**Fecha:** 2026-09-28
**Alcance:** todo documento HTML autocontenido (guía gráfica, landing, resumen visual) generado dentro de cualquier proyecto de HMG (Hospital HMG, verticales de marca, business plans, propuestas web).
**Referencia canónica:** `https://hospitalhmg.com/trasplante-hepatico.html`

## Regla dura

Toda guía gráfica o landing nueva de HMG debe usar el sistema de diseño **claro** de `hospitalhmg.com/trasplante-hepatico.html`, **no** el tema oscuro genérico del skill global `guia-grafica` (`~/.config/devin/skills/guia-grafica/SKILL.md`). El skill global sigue siendo válido para su propósito general (corpus de conocimiento no relacionados con HMG), pero cuando el resultado es para HMG, se combinan sus principios pedagógicos (badges de evidencia, cero datos ficticios, trazabilidad) con **estos tokens visuales**, no con su paleta oscura por defecto.

## Design tokens (copiar literalmente)

```css
:root {
  --hmg-teal: #007481;
  --hmg-teal-dark: #005f6b;
  --hmg-teal-light: #7ebec5;
  --hmg-blue: #2ea3f2;
  --bg: #ffffff;
  --surface: #f7f9fa;
  --text: #1a2a2e;
  --muted: #5b6b6f;
  --amber: #b5651d;
  --amber-bg: #fff4e8;
  --danger: #b42318;
  --danger-bg: #fff0f0;
  --radius: 14px;
  --shadow: 0 10px 30px rgba(0,0,0,0.07);
  --max-width: 1160px;
}
body { font-family:"Open Sans","Inter",system-ui,-apple-system,BlinkMacSystemFont,sans-serif; }
```

- **Tipografía:** Open Sans (cuerpo) + Inter (apoyo), vía Google Fonts.
- **Tema:** claro, fondo blanco, superficies `--surface` gris muy claro. Nunca fondo oscuro.
- **Header:** sticky, translúcido con blur, solo logo (sin texto redundante junto al logo — ver incidente 2026-09-28 donde apareció "HMG" duplicado junto al logo, corregido).
- **Botones:** `border-radius: 999px` (pill), `--hmg-teal` sólido para primario, borde teal para secundario.
- **Secciones:** alternar fondo blanco / `--surface` para separar visualmente, `border-bottom` sutil.
- **Tablas:** bordes `rgba(0,116,129,0.12)`, encabezado en `--surface` con texto `--hmg-teal-dark`.
- **Badges de evidencia:** usar el patrón de 4 colores (verificado/estimación/dato primario/riesgo) con fondos pastel, no colores saturados de neón.

## Gráficos y diagramas: usar IA, no SVG a mano

**Regla dura (incidente 2026-09-28):** los diagramas SVG hechos a mano con `<text>` largo y sin ajuste de línea produjeron texto sobrepuesto e ilegible. La corrección con `foreignObject` resolvió la superposición pero la calidad visual seguía siendo insuficiente para el estándar HMG.

**En su lugar:** generar cada gráfico/infografía con el skill `gpt-image-2` (`~/.config/devin/skills/gpt-image-2/SKILL.md`), que usa `openai-image-gen.generate_image_gpt2` con una plantilla de 6 bloques (tipo de imagen + técnica, paleta exacta en hex, layout nodo-a-nodo con texto exacto entre comillas, iconografía de apoyo, candados de legibilidad, restricciones negativas). Parámetros fijos: `size: "1536x1024"`, `quality: "high"`, `output_format: "png"`. Nunca usar `generate_image_gpt2_thinking` (bug conocido: error 400 "Unknown parameter: 'thinking'").

Insertar como `<img class="diagram-img" src="..." loading="lazy" />` dentro de un `.diagram-wrap`, con `<p class="diagram-caption">` citando la fuente exacta debajo.

## Fotografía

Mismo mecanismo (`gpt-image-2` / `openai-image-gen`), con lineamientos éticos específicos ya establecidos para contenido médico pediátrico sensible (ver `PROPUESTA_HMG_TRASPLANTE_HEPATICO/HMG_TRASPLANTE_HEPATICO_ESTUDIO_Y_BUSINESS_PLAN.md`, sección C1): nunca mostrar niños que parezcan enfermos, nunca prometer resultado visualmente, nunca escenas quirúrgicas explícitas.

## Referencias de implementación

| Documento | Rol |
|---|---|
| `hospitalhmg-homepage/trasplante-hepatico.html` | Referencia canónica pública, landing con el sistema de diseño completo |
| `PROPUESTA_HMG_TRASPLANTE_HEPATICO/GUIA_GRAFICA_HMG_TRASPLANTE_HEPATICO.html` | Primera guía gráfica reconstruida bajo este estándar (2026-09-28) |
| `~/.config/devin/skills/gpt-image-2/SKILL.md` | Cómo generar cada gráfico/foto |
| `~/.config/devin/skills/guia-grafica/SKILL.md` | Principios pedagógicos generales (badges, trazabilidad) — combinar con estos tokens, no con su tema oscuro |

## Próximas guías gráficas

Antes de generar cualquier nueva guía gráfica o landing para HMG, leer este documento primero y copiar los tokens CSS literalmente desde `trasplante-hepatico.html` (no reinventar la paleta ni la tipografía).
