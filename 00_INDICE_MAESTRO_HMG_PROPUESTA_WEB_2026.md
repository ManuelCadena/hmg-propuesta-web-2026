# Índice Maestro — Propuesta Web Pública HMG 2026

**Ubicación:** `/Users/manuelcadena/My Drive/Manuel Cadena/New Life/APPS/HMG/PROPUESTA_WEB_HMG_2026/`  
**Caso/APP:** Hospital HMG (Hospital Medical Group / Hospital HMG Coyoacán)  
**Fecha de creación:** 2026-09-27  
**Propósito:** Centralizar todos los entregables de la propuesta de sitio web informativo público para hospitalhmg.com.

---

## Entregables principales

| Archivo | Descripción | Estado |
|---|---|---|
| `PROPUESTA_WEB_HOSPITAL_HMG_2026.md` | Documento maestro con estrategia, arquitectura, homepage, workflow, directorio médico, identidad HMG, integración LINA, botón CRM, prompts de imágenes, KPIs, riesgos y glosario. | Completado |
| `GUÍA_GRAFICA_PROPUESTA_WEB_HMG.html` | Guía visual autocontenida con el flujo del paciente, arquitectura del sitio y aplicación de marca. | Completado |
| Vista previa local | http://127.0.0.1:8765/GUIA_GRAFICA_PROPUESTA_WEB_HMG.html | Servidor activo |
| `assets/logo_hmg_historico.webp` | Logo extraído del sitio histórico `hmghospital.com.mx` para referencia de marca. | Guardado |
| `assets/` | Carpeta para imágenes generadas con IA, favicon y otros recursos visuales futuros. | Creada |
| `assets/img_hero_exterior.png` | Hero de homepage: exterior hospital moderno, paleta HMG. | Generado (OpenAI gpt-image-1-mini) |
| `assets/img_atencion_humana.png` | Imagen de consulta médica con empatía. | Generado (OpenAI gpt-image-1-mini) |
| `assets/img_tecnologia_precision.png` | Tecnología médica e innovación. | Generado (OpenAI gpt-image-1-mini) |
| `assets/img_equipo_multidisciplinario.png` | Equipo de profesionales de salud. | Generado (OpenAI gpt-image-1-mini) |
| `assets/img_bienestar_prevencion.png` | Bienestar y atención preventiva. | Generado (OpenAI gpt-image-1-mini) |
| MCP `together-image-gen` | Servidor MCP para generación de imágenes con Together AI (FLUX). | Configurado; prueba falló por credenciales/expiración |
| MCP `openai-image-gen` | Servidor MCP para generación de imágenes con OpenAI (DALL-E / gpt-image). | Configurado y operativo |

---

## Fuentes y evidencia consultada

1. **Contrato de Licencia de Uso No Exclusiva y Gratuita de Signos Distintivos**  
   `20260923_NCR_Contrato_Licencia_HMG_v1 (1).docx` — convertido a `20260923_NCR_Contrato_Licencia_HMG_v1_VISTA_PREVIA.md`.
2. **Base de datos HMG Medical CRM** (`medicos_hmg.db`) — 3,382 médicos, 2,517 credencializados.
3. **Benchmarking web**:
   - Mayo Clinic: https://www.mayoclinic.org/
   - Cleveland Clinic: https://my.clevelandclinic.org/
   - Intermountain Health: https://intermountainhealthcare.org/
   - Hospital Angeles: https://hospitalangeles.com/
   - Centro Médico ABC: https://centromedicoabc.com/
   - Médica Sur: https://www.medicasur.com.mx/
   - Sitio histórico HMG: https://hmghospital.com.mx/
4. **Investigación académica** vía Consensus: triage en atención primaria, patient navigation, online triage tools, patient journey mapping.
5. **Análisis de tendencias** vía Perplexity Sonar Pro: state of the art en sitios médicos 2025-2026.
6. **Arquitectura del CRM HMG** (`hmg-crm/docs/ARCHITECTURE.md`, `ARQUITECTURA_AGENTES_LINA.md`, `LINAWidget.jsx`).

---

## Siguientes pasos sugeridos

1. Revisar y aprobar la propuesta con el equipo directivo y asesoría legal de HMG.
2. Validar con cada médico la publicación de sus datos de contacto en el directorio.
3. Configurar el agente LINA para uso público con controles de privacidad, consentimiento y fallback.
4. Generar las imágenes con IA usando los prompts entregados (DALL-E, Midjourney, Stable Diffusion, etc.).
5. Desarrollar prototipo en Figma o código en React y realizar pruebas de usuario.
6. Implementar, medir KPIs y iterar.

---

## Control de versiones

| Versión | Fecha | Cambios | Autor |
|---|---|---|---|
| 1.0 | 2026-09-27 | Creación del índice y documento maestro. | Devin |
