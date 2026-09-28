# SOURCE_OF_TRUTH — Propuesta Web Pública HMG 2026

**Caso/APP:** Hospital HMG (Hospital Medical Group / Hospital HMG Coyoacán)  
**Dominio:** hospitalhmg.com  
**Última actualización:** 2026-09-28  

---

## 1. Decisión de producto aprobada

El sitio público hospitalhmg.com será un **punto de acceso a la atención médica**, no un folleto institucional. Tres caminos principales:

1. **Paciente:** encuentra médico por especialidad o síntoma, obtiene orientación con LINA y contacta directamente al profesional.
2. **Contenido:** páginas SEO por especialidad y servicio.
3. **Médicos/Staff:** acceso al CRM privado.

## 2. Restricciones legales y de marca

- HMG (New Century Real Estate, S. de R.L. de C.V.) licencia signos distintivos a profesionales independientes; no es operador hospitalario ni empleador de los médicos.
- Cada servicio publicado debe identificar al profesional independiente que lo presta.
- El uso de signos distintivos sigue el Contrato de Licencia de Uso No Exclusiva y Gratuita de Signos Distintivos, Anexos A, B y C.
- Los datos de contacto de médicos se publican con **autorización expresa** para fines publicitarios de sus servicios.

## 3. Arquitectura aprobada

```
hospitalhmg.com
├── Inicio
├── Encuentra a tu médico (por especialidad, síntoma, nombre)
├── Especialidades y servicios
├── Orientación con LINA
├── Para pacientes
├── Para médicos (con botón al CRM)
└── HMG (legal, privacidad, contacto)
```

## 4. Workflow aprobado

1. El paciente expresa síntoma, especialidad o nombre.
2. **Filtro de urgencia:** si hay señales de alarma, se detiene y se instruye llamar al 911 o ir a urgencias.
3. Orientación segura (sin diagnóstico) hacia especialidad o médico.
4. Selección de médico con datos verificables.
5. Contacto o captura de intención de cita con consentimiento.
6. Confirmación por canal seguro.

## 5. Seguridad de LINA público

- LINA en la web pública solo navega, orienta y canaliza contactos.
- No diagnostica, no prescribe, no interpreta estudios, no modifica medicación.
- Captura solo datos mínimos con consentimiento explícito.
- Endpoints públicos aislados en `/api/elevenlabs-public`, sin acceso a datos sensibles de pacientes, proveedores o aseguradoras.
- Fallback a humano y a emergencias ante cualquier situación clínica o de duda.

## 6. Repositorios oficiales

| Recurso | URL |
|---|---|
| CRM HMG (código + LINA blindado) | https://github.com/ManuelCadena/hmg-crm |
| Propuesta web, guía gráfica e imágenes | https://github.com/ManuelCadena/hmg-propuesta-web-2026 |

## 7. Assets oficiales

- Logo histórico HMG: `assets/logo_hmg_historico.webp`
- Imágenes generadas con IA: `assets/img_hero_exterior.png`, `img_atencion_humana.png`, `img_tecnologia_precision.png`, `img_equipo_multidisciplinario.png`, `img_bienestar_prevencion.png`
- Paleta primaria: `#007481`

## 8. Estado de despliegue

| Componente | Estado | URL |
|---|---|---|
| Homepage estática | DEPLOY-VERIFICADO | https://hospitalhmg.com |
| API pública LINA | DEPLOY-VERIFICADO | https://hospitalhmg.com/api/elevenlabs-public |
| CRM interno | Operativo | https://crm.hospitalhmg.com/crm/login |
| DNS A records | Creados en Route 53 | hospitalhmg.com / www → 44.247.163.1 |
| Certificado SSL | Let's Encrypt activo | /etc/letsencrypt/live/hospitalhmg.com |

## 9. Próximos pasos

1. Validar imágenes generadas con el equipo de marca.
2. Verificar resolución global del dominio en todos los resolvers.
3. Añadir directorio interactivo de médicos (React) consumiendo `/api/elevenlabs-public`.
4. Implementar analytics, consentimiento explícito y auditoría de conversaciones LINA.
5. Realizar pruebas de usuario y accesibilidad.
