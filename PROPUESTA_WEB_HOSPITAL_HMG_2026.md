# Propuesta de Sitio Web Público para Hospital HMG

**Versión:** 1.0  
**Fecha:** 2026-09-27  
**Dominio:** hospitalhmg.com  
**Objetivo:** Diseñar una experiencia web pública limpia, funcional y orientada a la conversión, que promueva los servicios de los médicos independientes asociados a HMG bajo la licencia de signos distintivos, facilite el contacto y agende atención, e integre el agente LINA como interfaz conversacional.

---

## 1. Resumen ejecutivo

La propuesta redefine hospitalhmg.com como un **punto de acceso a la atención médica**, no como un folleto institucional. El sitio conecta a tres audiencias: pacientes que buscan orientación o un especialista, médicos que desean gestionar su presencia, y el equipo interno que opera el CRM.

La estrategia se basa en evidencia de Mayo Clinic, Cleveland Clinic, Intermountain Health, Centro Médico ABC, Hospital Angeles y Médica Sur: hero orientado a la acción, navegación de máximo tres a cinco elementos, directorio médico filtrable por especialidad y síntoma, y un agente conversacional que guía sin diagnosticar.

El sitio debe:

1. Responder en menos de tres segundos qué hace HMG y cuál es el siguiente paso.
2. Permitir buscar médicos por especialidad, padecimiento, procedimiento o nombre.
3. Ofrecer orientación segura mediante LINA (chat y voz) con escalamiento a humano.
4. Facilitar el contacto directo: WhatsApp, teléfono o enlace al CRM del médico.
5. Respetar escrupulosamente la naturaleza de la licencia: HMG licencia signos distintivos a profesionales independientes; no opera un hospital como franquicia.
6. Incluir un botón de acceso al CRM actual en el área privada.

---

## 2. Posicionamiento de marca y propuesta de valor

### Posicionamiento

**HMG: atención médica confiable y cercana en el sur de la Ciudad de México.**

### Mensaje rector

> Encuentra la atención médica que necesitas, cerca de ti y con orientación clara.

### Propuesta de valor

- **Cerca:** ubicación física en Coyoacán y énfasis en el sur de la Ciudad de México.
- **Confiable:** profesionales independientes con información de cédula profesional, especialidad y credencialización publicada.
- **Claro:** un flujo que va del síntoma a la especialidad y del especialista al contacto, sin diagnósticos automáticos ni promesas de resultados.

### Audiencias

| Audiencia | Necesidad | Mensaje clave |
|---|---|---|
| Paciente con síntoma | Saber con qué especialista acudir | "¿No sabes con qué especialista acudir? LINA te orienta." |
| Paciente con especialista buscado | Contactar o agendar rápido | "Encuentra a tu médico y contáctalo directamente." |
| Médico asociado | Gestionar su presencia y citas | "Haz crecer tu consulta con las herramientas digitales de HMG." |
| Personal/administrativo | Acceder al CRM | "Acceso al CRM" |

---

## 3. Arquitectura de información

```
hospitalhmg.com
├── Inicio
├── Encuentra a tu médico
│   ├── Por especialidad
│   ├── Por síntoma o padecimiento
│   ├── Por procedimiento
│   └── Directorio completo
├── Especialidades y servicios
│   ├── Especialidades destacadas
│   └── Servicios médicos amparados
├── Orientación con LINA
├── Para pacientes
│   ├── Cómo agendar
│   ├── Telemedicina
│   ├── Preguntas frecuentes
│   ├── Preparación para consulta
│   └── Urgencias
├── Para médicos
│   ├── Beneficios de asociarte
│   ├── Licencia de uso de signos
│   └── Acceso al CRM
├── HMG
│   ├── Identidad y ubicación
│   ├── Aviso de privacidad
│   ├── Términos y condiciones
│   └── Contacto
```

**Reglas de navegación:**

- Header persistente con logo, buscador, "Encuentra a tu médico", "Especialidades", "Orientación con LINA", "Contacto" y botón "Acceso al CRM".
- En móvil, los botones fijos inferiores son: "Buscar médico", "LINA" y "Llamar".
- Pie de página con aviso de privacidad, disclaimer médico, teléfono de urgencias, aviso comercial y datos de contacto de HMG.

---

## 4. Estructura de la homepage

| Sección | Copy propuesto | CTA principal | Justificación de conversión |
|---|---|---|---|
| **Header** | HMG Hospital Coyoacán · Atención médica cerca de ti | Encuentra a tu médico | Reduce fricción: la acción más frecuente está visible sin scroll. |
| **Hero** | *La atención médica que necesitas, más cerca de ti.* Encuentra especialistas, conoce tus opciones y contacta a profesionales independientes vinculados a HMG. | Buscar médico / Hablar con LINA | Responde las dos intenciones principales: búsqueda directa y orientación. |
| **Buscador** | Encuentra a tu médico por especialidad, padecimiento o nombre. | Buscar | Capta tráfico con intención alta y mejora SEO. |
| **Orientación LINA** | ¿No sabes con qué especialista acudir? LINA puede orientarte. | Hablar con LINA | Convierte dudas en navegación guiada; no reemplaza diagnóstico. |
| **Especialidades destacadas** | Ginecología y Obstetricia · Anestesiología · Cirugía General · Pediatría · Ortopedia · Medicina Interna · Cardiología | Ver todas las especialidades | Muestra la oferta más amplia del directorio. |
| **Servicios** | Consultas · Cirugía · Telemedicina · Análisis médicos · Fisioterapia · Reserva de citas | Explorar servicios | Comunica el alcance permitido por la licencia. |
| **Confianza** | Profesionales independientes con información verificable. Consulta especialidad, cédula y datos de contacto publicados. | Conocer criterios | Refuerza transparencia y autonomía profesional. |
| **Ubicación** | Hospital HMG Coyoacán. Cerca de ti, cerca de todos. | Cómo llegar | Refuerza el aviso comercial registrado y la cercanía geográfica. |
| **Para médicos** | Haz crecer tu presencia profesional con las herramientas digitales de HMG. | Soy médico / Acceder al CRM | Separa audiencias y envía al CRM. |
| **Footer** | Aviso de privacidad · Términos · Disclaimer médico · Urgencias · Contacto | - | Cumplimiento y confianza. |

**Disclaimer visible recomendado:**

> La información de este sitio es general y no sustituye una consulta médica. HMG facilita orientación y conexión con profesionales independientes. En una emergencia, llama al 911 o acude al servicio de urgencias más cercano.

---

## 5. Workflow del paciente: síntoma → atención → resolución

El flujo está diseñado a partir de la investigación académica revisada: el patient navigation mejora acceso y resultados; el triage en línea acelera decisiones pero debe evitar diagnósticos definitivos y escalonar emergencias de inmediato.

| Paso | Experiencia | Canal | Decisión de seguridad |
|---|---|---|---|
| 1. Expresar necesidad | El usuario describe un síntoma, padecimiento, procedimiento o especialidad. | Web, chat LINA, voz LINA | LINA declara que no diagnostica. |
| 2. Filtro de urgencia | Se detectan señales de alarma: dificultad respiratoria, dolor torácico intenso, pérdida de conciencia, sangrado abundante, síntomas neurológicos súbitos, embarazo con complicaciones. | Chat, voz o formulario | Si hay señales de alarma, se interrumpe el flujo y se muestra: **llama al 911 o acude a urgencias**. |
| 3. Orientación segura | LINA o el buscador sugiere una **especialidad o ruta de atención** usando lenguaje probabilístico: "Para este síntoma, muchos pacientes consultan con...". | Web, chat, voz | No se emite diagnóstico, pronóstico ni prescripción. |
| 4. Selección de médico | El usuario filtra por especialidad, ubicación, modalidad, disponibilidad y credenciales publicadas. | Directorio web | Se indica que cada médico es profesional independiente. |
| 5. Contacto o agendamiento | Se ofrece llamada telefónica, WhatsApp o enlace al sistema de citas del médico. | Web, WhatsApp, teléfono | Solo se solicitan datos mínimos; se muestra aviso de privacidad. |
| 6. Confirmación | Se confirma médico, fecha, modalidad, dirección y documentos requeridos. | Correo, SMS, WhatsApp | Se registra consentimiento y se evita enviar datos clínicos por canales inseguros. |
| 7. Atención médica | Consulta presencial o telemedicina con el profesional seleccionado. | Presencial o videollamada | El diagnóstico y tratamiento son responsabilidad exclusiva del médico. |
| 8. Continuidad | Recordatorio, reprogramación o información de seguimiento según el médico. | CRM, correo, canal autorizado | La información clínica se maneja solo entre paciente y médico. |

---

## 6. Directorio médico

### Campos de perfil público

Cada tarjeta de médico debe mostrar:

- Nombre completo.
- Especialidad principal y subespecialidades.
- Cédula profesional (opcional, según autorización del médico).
- Consultorio o ubicación de atención.
- Modalidad: presencial, telemedicina o ambas.
- Teléfono de contacto.
- Correo electrónico o formulario de contacto.
- Horario de atención (si aplica).
- Breve biografía profesional.
- Botones: "Llamar", "WhatsApp", "Agendar cita".
- Leyenda visible: *Profesional independiente. Datos publicados bajo su responsabilidad.*

### Filtros del directorio

- Especialidad.
- Síntoma o padecimiento.
- Procedimiento.
- Ubicación.
- Modalidad (presencial / telemedicina).
- Disponibilidad.
- Idioma.

### Ejemplos de perfiles (datos reales del CRM, mostrados como muestra)

| Nombre | Especialidad | Contacto | Modalidad |
|---|---|---|---|
| Abarca Mass Raymundo | Cirugía General | 55 1392 7944 | Por confirmar |
| Abarca Matus María Eloisa | Otorrinolaringología | 55 5419 7883 | Por confirmar |
| Abarca Pérez Leonardo | Cirugía General, Cirugía Plástica y Reconstructiva | 55 5105 2123 | Por confirmar |
| Abdo Francis Juan Miguel | Gastroenterología, Endoscopia del Aparato Digestivo | 55 5404 5409 | Por confirmar |

> Estos ejemplos provienen de la base de datos HMG. El directorio final publicará únicamente la información que cada médico autorice y valide.

---

## 7. Mapa de especialidades y servicios a promover

### Top 15 especialidades por número de médicos

| Orden | Especialidad | Médicos en CRM |
|---:|---|---:|
| 1 | Ginecología y Obstetricia | 423 |
| 2 | Anestesiología | 418 |
| 3 | Cirugía General | 396 |
| 4 | Pediatría | 252 |
| 5 | Ortopedia y Traumatología | 249 |
| 6 | Medicina Interna | 233 |
| 7 | Cardiología | 127 |
| 8 | Neurocirugía | 94 |
| 9 | Urología | 85 |
| 10 | Otorrinolaringología | 78 |
| 11 | Gastroenterología | 55 |
| 12 | Cirugía Plástica y Reconstructiva | 52 |
| 13 | Oncología | 49 |
| 14 | Neonatología | 46 |
| 15 | Neumología | 37 |

### Especialidades secundarias

Nefrología, Neurología, Radiología e Imagen, Endocrinología, Dermatología, Oftalmología, Psiquiatría, Reumatología, Infectología, Hematología.

### Servicios médicos amparados por la licencia (clase 44)

- Consultas médicas.
- Cirugía.
- Cirugía estética y plástica.
- Análisis médicos.
- Fisioterapia.
- Reserva de citas.
- Telemedicina.
- Servicios hospitalarios.
- Asesoramiento médico.
- Exploración médica.
- Facilitación de información sobre salud.
- Servicios de clínicas médicas.
- Servicios de psicólogos.
- Servicios de enfermeros.

> Cada servicio se publicará como prestado por un profesional independiente específico. HMG no presta directamente los servicios ni garantiza resultados.

---

## 8. Identidad de marca HMG en la web

### Signos distintivos disponibles

| Signo | Variación principal | Uso recomendado en web |
|---|---|---|
| HMG | Denominación nominativa | Header, favicon, pie de página, etiquetas. |
| HMG Hospital Coyoacán y diseño | Signo mixto a color o tinta | Hero, encabezados institucionales, papelería digital. |
| HMG Torre Médica | Denominación nominativa | Sección para médicos, Torre Médica. |
| HMG Tu Opción en el Sur | Denominación nominativa | Campañas locales, sur de la Ciudad de México. |
| Cerca de ti, cerca de todos | Aviso comercial | Footer, banners de cercanía, campañas de confianza. |

### Reglas de uso digital

- Logotipo mínimo: **120 px de ancho**.
- Espacio libre alrededor del signo: equivalente, al menos, a la altura de la letra H.
- Colores originales o una sola tinta: negro, blanco o escala de grises.
- No deformar, recortar, rotar ni alterar proporciones.
- Nombre y especialidad del médico deben ubicarse en bloque separado, sin fusionarse con el logotipo.
- Usar **M.R.** o **®** según el signo y servicio amparado.

### Paleta de colores sugerida (basada en sitio histórico y marca)

| Token | Uso | Valor HEX |
|---|---|---|
| Primary | Headers, CTAs, acentos | `#007481` |
| Primary Light | Fondos suaves, hover | `#7EBEC5` |
| Primary Dark | Texto sobre fondos claros | `#005F6B` |
| Accent | Botones secundarios, links | `#2EA3F2` |
| Background | Fondo general | `#FFFFFF` |
| Surface | Tarjetas, secciones alternas | `#F8FAFA` |
| Text Primary | Cuerpo | `#333333` |
| Text Secondary | Subtítulos | `#666666` |
| Border | Bordes sutiles | `#E5E5E5` |
| Urgency | Alertas de emergencia | `#C0392B` |

### Tipografía

- **Encabezados:** una fuente serif o humanista (p. ej., Georgia, Rector o similar) para transmitir calidez y autoridad.
- **Cuerpo:** Open Sans, system-ui o Inter, por legibilidad digital y accesibilidad.
- **Tamaños mínimos:** 16 px para cuerpo, 18 px para botones, 24 px para H2.

### Ejemplo de aplicación en tarjeta médica

```
[LOGO HMG Hospital Coyoacán]  (mínimo 120 px, espacio libre)

---

Dra. María López Herrera
Ginecología y Obstetricia
Cédula Profesional: 12345678
Consultorio 305, HMG Torre Médica
Tel. 55 1234 5678
WhatsApp | Agendar cita

Profesional independiente.
```

---

## 9. Integración del agente LINA en la página pública

### Objetivo

LINA es el asistente virtual de HMG. En la web pública orienta, busca en el directorio y canaliza contactos, sin diagnosticar.

### Ubicación

- Botón flotante persistente en la esquina inferior derecha: **"Habla con LINA"**.
- Acceso adicional en el hero: **"¿No sabes con qué especialista acudir?"**.
- Modal inicial con consentimiento y aviso de privacidad.

### Modos

- **Chat:** texto con respuestas rápidas.
- **Voz:** mediante ElevenLabs Conversational AI, útil para usuarios que prefieren hablar.

### Flujo de inicio

1. "Soy LINA, el asistente virtual de HMG. No sustituyo a un profesional de la salud."
2. "¿Buscas un médico, tienes un síntoma o necesitas información de servicios?"
3. Si el usuario describe un síntoma, LINA pregunta por señales de alarma antes de sugerir especialidad.
4. LINA muestra opciones del directorio o enlaces de contacto.
5. Ante cualquier duda clínica o emergencia, deriva a un humano o indica llamar al 911.

### Funciones permitidas

- Buscar especialidades y médicos.
- Explicar servicios, modalidades y formas de contacto.
- Orientar sobre el proceso general de agenda.
- Capturar datos mínimos de contacto previo consentimiento.
- Transferir a humano.

### Funciones prohibidas

- Diagnosticar, prescribir, interpretar estudios o recomendar medicación.
- Prometer disponibilidad, resultados, costos o tiempos no confirmados.
- Solicitar datos bancarios, contraseñas o información clínica innecesaria.

### Fallback

| Situación | Acción |
|---|---|
| Fallo técnico | Mostrar teléfono, formulario y horario de atención. |
| Pregunta no reconocida | "No puedo confirmar esa información. Permíteme derivarte a un representante de HMG." |
| Contenido clínico o urgente | Detener la conversación clínica y recomendar atención profesional inmediata. |
| Solicitud de datos sensibles | Rechazar la captura y redirigir al canal seguro. |

### Snippet conceptual para insertar widget ElevenLabs en React

```jsx
import { useEffect } from 'react';

export default function LINAWidget() {
  useEffect(() => {
    if (document.querySelector('script[src*="elevenlabs"]')) return;
    const widget = document.createElement('elevenlabs-convai');
    widget.setAttribute('agent-id', 'agent_2001kgkn3s4cek0rk9y0m7qcbtn9');
    document.body.appendChild(widget);
    const script = document.createElement('script');
    script.src = 'https://unpkg.com/@elevenlabs/convai-widget-embed';
    script.async = true;
    document.body.appendChild(script);
    return () => {
      widget.remove();
      script.remove();
    };
  }, []);
  return null;
}
```

> El agent-id coincide con el componente actual del CRM. Antes del lanzamiento público se debe validar que el agente tenga permisos de consulta pública, política de retención de datos y consentimiento configurados.

---

## 10. Botón de acceso al CRM

**URL destino:** `https://crm.hospitalhmg.com/crm/login`

### Ubicación

- Escritorio: header superior derecho, junto a "Contacto".
- Móvil: menú desplegable, sección "Área de médicos y personal".
- Pie de página: enlace secundario.
- Página "Para médicos": botón principal.

### Rol

Acceso privado para personal autorizado, médicos y coordinadores. No es un portal para pacientes.

### Copy recomendado

- Botón: **Acceso al CRM**
- Texto auxiliar: **Portal exclusivo para personal autorizado**
- Tooltip: **Iniciar sesión en el CRM de HMG**

---

## 11. Imágenes generadas con IA

No se dispone de un generador de imágenes directo en este entorno; por ello se entregan prompts profesionales listos para usarse con DALL-E, Midjourney, Stable Diffusion u otra herramienta de generación de imágenes.

### Paleta recomendada para las imágenes

- Verde azulado profundo: `#007481`
- Verde azulado claro: `#7EBEC5`
- Blanco: `#FFFFFF`
- Gris oscuro: `#333333`
- Azul de acento: `#2EA3F2`

### Prompts

1. **Hero exterior**
   > Premium editorial photograph of a modern private medical building exterior, welcoming entrance, warm natural daylight, diverse patients and healthcare professionals walking, subtle teal and white color palette (#007481, #7EBEC5), calm and trustworthy atmosphere, realistic photography, generous negative space for website copy, no readable text, no logos, no specific faces, 16:9.

2. **Atención médica humana**
   > Authentic healthcare scene in a bright modern consultation room, compassionate physician speaking with an adult patient, respectful eye contact, natural gestures, diverse representation, soft daylight, sophisticated teal, white and blue palette, reassuring and professional mood, realistic editorial photography, no medical diagnosis shown, no readable text, no logos, 4:3.

3. **Tecnología y precisión**
   > High-end conceptual image representing advanced healthcare technology, physician reviewing digital medical data on a transparent interface, clean clinical environment, subtle teal and blue lighting, precision, innovation and trust, realistic but refined corporate healthcare style, no identifiable patient data, no readable text, no logos, 16:9.

4. **Equipo multidisciplinario**
   > Diverse multidisciplinary healthcare team walking through a bright modern hospital corridor, confident yet approachable, coordinated professional attire, authentic collaboration, premium corporate healthcare photography, teal and white palette inspired by #007481, soft natural light, realistic expressions, no readable signage, no logos, 16:9.

5. **Bienestar y prevención**
   > Elegant healthcare lifestyle image showing an adult patient receiving preventive care guidance from a healthcare professional, bright consultation space, optimistic but not exaggerated, inclusive representation, clean teal and white brand palette, natural light, premium editorial photography, realistic skin texture, no readable text, no logos, 16:9.

---

## 12. Recomendaciones técnicas de implementación

### Stack sugerido

- **Frontend:** React + Vite + Tailwind CSS (consistente con el CRM actual).
- **Backend:** API REST con Express.js y PostgreSQL (reutilizar capa del CRM).
- **Búsqueda:** endpoint `/api/medicos` con filtros por especialidad, síntoma y nombre.
- **Agente:** widget ElevenLabs Conversational AI.
- **Hosting:** Vercel/Netlify para frontend; servidor actual del CRM para API.
- **Analytics:** Google Analytics 4 con eventos de conversión sin datos clínicos.

### SEO

- Meta título: "Hospital HMG Coyoacán | Encuentra médicos especialistas en el sur de CDMX".
- Meta descripción con especialidades principales.
- URLs semánticas: `/especialidades/ginecologia`, `/medicos/`, `/servicios/`.
- Schema.org: MedicalWebPage, Physician, MedicalClinic, Hospital.
- Sitemap y robots.txt.

### Accesibilidad

- Cumplimiento con WCAG 2.1 nivel AA.
- Contraste mínimo 4.5:1.
- Navegación por teclado.
- Etiquetas ARIA en buscador, botones y formularios.
- Texto alternativo en imágenes.

### Performance

- Imágenes en WebP con lazy loading.
- Fuentes autoalojadas o precargadas.
- Caché de API y paginación en directorio.
- Core Web Vitales objetivo: LCP < 2.5 s, INP < 200 ms, CLS < 0.1.

### Seguridad

- HTTPS obligatorio.
- CSP restrictivo para scripts de terceros.
- Aviso de privacidad visible antes de recabar datos.
- No exponer información clínica en respuestas públicas de API.
- Logs sin datos sensibles.

---

## 13. KPIs y plan de medición

### KPIs principales

| Área | KPI | Método |
|---|---|---|
| Conversión | Clics en "Contactar" / "Agendar" | Eventos GA4 + CRM |
| Directorio | Búsquedas y filtros usados | GA4 + logs de API |
| LINA | Conversaciones iniciadas | ElevenLabs analytics |
| LINA | Resolución sin intervención humana | Registro del agente |
| LINA | Tasa de escalamiento | Transferencias a humano |
| CRM | Clics en "Acceso al CRM" | Evento GA4 separado |
| Experiencia | CSAT | Encuesta posterior a interacción |
| Rendimiento | Tiempo de carga y disponibilidad | Lighthouse + uptime monitor |
| Accesibilidad | Errores WCAG | Auditoría mensual |
| Calidad | Respuestas incorrectas o incidentes | Revisión humana semanal |

### Plan de medición

1. Definir eventos y objetivos antes del lanzamiento.
2. Implementar GA4 con consentimiento y sin datos clínicos.
3. Etiquetar por página, dispositivo, idioma y campaña.
4. Lanzar prueba piloto con personal HMG y usuarios controlados.
5. Revisar semanalmente conversiones, errores y escalamiento durante el primer mes.
6. Auditar mensualmente una muestra de conversaciones de LINA.
7. A/B testing solo en elementos no clínicos: copy, ubicación y diseño de botones.

---

## 14. Riesgos legales, éticos y mitigaciones

| Riesgo | Mitigación |
|---|---|
| El usuario confunde a LINA con un profesional de salud | Identificación visible como IA, aviso de limitaciones, acceso a atención humana. |
| Diagnóstico o consejo médico incorrecto | Bloqueo de consultas clínicas individualizadas, base de conocimiento aprobada, pruebas adversariales. |
| Exposición de datos personales o de salud | Minimización de datos, cifrado, control de acceso, retención limitada, aviso de privacidad. |
| Transferencia internacional de datos | Revisión contractual y configuración regional de proveedores. |
| Grabación o transcripción sin consentimiento | Aviso previo, consentimiento cuando aplique, desactivación de grabaciones innecesarias. |
| Información desactualizada sobre servicios, horarios o precios | Propietario interno de contenidos, fecha de actualización, derivación cuando exista duda. |
| Discriminación o accesibilidad insuficiente | Pruebas con distintos perfiles, lenguaje inclusivo, compatibilidad con tecnologías de asistencia. |
| Confusión sobre la naturaleza de HMG | Texto claro: HMG licencia signos distintivos; los médicos son profesionales independientes. |
| Uso incorrecto de los signos distintivos | Aplicar manual de marca, revisiones de compliance, espacio libre, colores y leyendas registradas. |

---

## 15. Glosario de siglas

| Sigla | Significado |
|---|---|
| **API** | Application Programming Interface (Interfaz de Programación de Aplicaciones). |
| **CAE** | Clínica de Alta Especialidad. |
| **CDMX** | Ciudad de México. |
| **CRM** | Customer Relationship Management; en este contexto, el sistema médico de HMG. |
| **CTA** | Call to Action (llamado a la acción). |
| **GA4** | Google Analytics 4. |
| **HMG** | Hospital Medical Group / Hospital HMG Coyoacán. |
| **IA** | Inteligencia Artificial. |
| **IMPI** | Instituto Mexicano de la Propiedad Industrial. |
| **INP** | Interaction to Next Paint, métrica de rendimiento web. |
| **LCP** | Largest Contentful Paint, métrica de rendimiento web. |
| **LGBTQ+** | Lesbian, Gay, Bisexual, Transgender, Queer/Questioning y otros. |
| **M.R.** | Marca Registrada. |
| **Niza** | Clasificación Internacional de Niza para productos y servicios. |
| **PIL** | Prueba de Interfaz de Lenguaje (en este contexto, pruebas de usuario). |
| **SEO** | Search Engine Optimization (optimización para motores de búsqueda). |
| **SMS** | Short Message Service (mensaje de texto). |
| **WCAG** | Web Content Accessibility Guidelines (pautas de accesibilidad web). |
| **WhatsApp** | Aplicación de mensajería instantánea. |

---

## 16. Referencias y fuentes

1. Contrato de Licencia de Uso No Exclusiva y Gratuita de Signos Distintivos, 04 de marzo de 2024. Anexos A, B y C.
2. Base de datos HMG Medical CRM: 3,382 médicos, 2,517 credencializados. Extraída el 2026-09-27.
3. Mayo Clinic: https://www.mayoclinic.org/ — estructura de navegación y hero "Healing starts here".
4. Cleveland Clinic: https://my.clevelandclinic.org/ — CTAs "Find a Provider", "Appointments", "Not Sure Where To Go for Care?".
5. Intermountain Health: https://intermountainhealthcare.org/ — hero "Let's look at health in a whole new way", find-a-doctor con filtros de disponibilidad y distancia.
6. Hospital Angeles: https://hospitalangeles.com/ — Directorio Médico y navegación simple.
7. Centro Médico ABC: https://centromedicoabc.com/ — "Encuentra a tu médico" por especialidad/padecimiento/procedimiento.
8. Médica Sur: https://www.medicasur.com.mx/ — énfasis en acreditaciones y calidez humana.
9. Sitio histórico HMG: https://hmghospital.com.mx/ — tipografía Open Sans, color primario aproximado `#007481`, logotipo HMG Hospital Coyoacán.
10. Park H, et al. "The Use of Triage in Primary Care in the UK: An Integrative Review and Narrative Synthesis." Journal of Advanced Nursing, 2025.
11. Park H, et al. "Scoping review of nurse triage in primary care." BMC Nursing, 2025.
12. Paule A, et al. "Patient-facing online triage tools and clinician decision-making: a systematic review." BMJ Open, 2025.
13. Chan R, et al. "Patient navigation across the cancer care continuum: An overview of systematic reviews and emerging literature." CA: A Cancer Journal for Clinicians, 2023.
14. Davies E, et al. "Reporting and conducting patient journey mapping research in healthcare: A scoping review." Journal of Advanced Nursing, 2022.
15. Perplexity Research: "State of the art 2025-2026 hospital website design and AI conversational agents in healthcare." 2026-09-27.

---

**Nota final:** Esta propuesta es un documento técnico y estratégico. Antes de su implementación, HMG debe validar la información médica y legal con sus asesores correspondientes, obtener la autorización expresa de cada médico para publicar sus datos de contacto, y configurar el agente LINA con los controles de privacidad y consentimiento requeridos.
