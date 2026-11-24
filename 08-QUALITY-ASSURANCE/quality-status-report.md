# Informe ejecutivo de estado de calidad

**Conclusión.** La base del producto permite continuar la investigación de campo y la definición de requisitos. Calidad recomienda mantener pendientes las aprobaciones de arquitectura, implementación, piloto y comercialización hasta que cada hito tenga su evidencia. Los once hallazgos A01–A11 siguen abiertos. La auditoría documental no estableció hallazgos críticos confirmados en el alcance revisado.

## Estado del proyecto y de las decisiones

| Estado | Contenido |
|---|---|
| Aprobado en el registro de `main` | Identidad registrada, mercado inicial Nicaragua, pequeños y medianos productores, ecosistema integral y desarrollo del collar por etapas. |
| Figura aprobado en el PR #2, pendiente de integración | Orientación comercial híbrida y prioridad de investigación y validación. Dirección debe precisar y ratificar su alcance en un registro trazable. |
| Propuesta técnica | PostgreSQL, NestJS, Next.js, aplicación móvil offline-first y arquitectura modular. Flutter y PowerSync son recomendaciones provisionales. Los controles de seguridad y recuperación son propuestas de diseño. |
| Pendiente de decisión | Alcance exacto del MVP, tecnologías definitivas, región, motor de sincronización, identidad y privacidad operativas, oferta, precios, condiciones comerciales y tipografía. Sensores y capacidades del collar requieren evaluación técnica. |

Base documental: [main a9eab9f](https://github.com/locurasdejose15-cloud/SAU-YUL-TECH-2.0/commit/a9eab9f49ac8df37e68626e3743bd17ea5280bb1) y [PR #2 de estrategia](https://github.com/locurasdejose15-cloud/SAU-YUL-TECH-2.0/pull/2). Se leyeron los siete documentos técnicos de la rama local `docs/technical-architecture` sobre `dee2ae5`. La revisión incorpora cambios locales sin commit en offline, seguridad y stack. Huellas SHA-256 abreviadas de las copias leídas, respectivamente: `c4780cc5f5d5`, `e09a38bf0aab`, `7fd04200c9bc`. Falta cotejar la propuesta UX/UI versionada. El detalle por archivo, responsables y criterios de cierre están en la [matriz](audit-findings-tracker.md).

## Riesgos que requieren decisión

- **Alcance y validación de campo · A02/A03.** Dirección necesita elegir con Producto qué problema y qué flujo justifican el MVP. Antes del trabajo de campo deben fijarse los criterios de evidencia, la composición de la muestra y el tratamiento de resultados adversos.
- **Offline e identidad · A06/A07.** La propuesta mitiga riesgos con cola durable, idempotencia, RLS y permisos de API. Los documentos difieren en el token del trabajador y en el tratamiento de los comandos pendientes tras revocar un teléfono. Antes de aprobar la arquitectura, unificar esos contratos y demostrar los escenarios excluyentes de la prueba de sincronización. Antes del piloto, repetir las pruebas en el candidato, incluida la separación entre fincas y organizaciones y la recuperación de un dispositivo revocado.
- **Capacidad y viabilidad · A05/A09.** El stack v2 incluye un perfil de piloto y estimaciones por entorno. Finanzas y Operaciones necesitan carga concurrente, picos de reconexión, mediciones reproducibles y costos verificables antes de comprometer la escala o la oferta. La estrategia híbrida requiere comprobar por separado el margen y la caja de software, hardware y servicios.
- **Oferta, accesibilidad y collar · A04/A08/A10.** La oferta visible debe corresponder a capacidades verificadas. Diseño debe probar legibilidad, estados de sincronización y recuperación. Si se incorpora hardware, aprobar seguridad animal y criterios de parada antes de probarlo en campo, y demostrar liberación del lote, trazabilidad y soporte antes de venderlo.

## Hitos pendientes

| Hito | Condición de avance |
|---|---|
| Requisitos del MVP | Evidencia de campo suficiente para seleccionar segmento y tarea principal. Alcance y permisos trazables a criterios de aceptación, con operaciones offline explícitas. |
| Arquitectura | Versión integrada de los siete documentos, decisión registrada para D-ARQ-06, contrato de identidad coherente, perfil de capacidad y plan de privacidad y validación. La prueba técnica de selección requiere alcance autorizado y datos sintéticos. |
| Inicio de implementación | Requisitos y arquitectura aprobados, criterios de recepción de código y diseño acordados, riesgos bloqueantes tratados y pruebas preparadas. |
| Piloto | Candidato versionado, protocolo de campo, permisos y tratamiento de datos aprobados, pruebas offline, aislamiento, rendimiento y accesibilidad superadas, soporte y restauración verificados. Aprobación específica si se usa el collar. |
| Comercialización | Resultados del piloto contrastados, precios y condiciones aprobados, costos sostenibles, promesas verificadas y capacidad de operación demostrada. El hardware requiere su expediente de liberación. |

**Decisión solicitada en esta revisión.** Ratificar los responsables y bloqueos de la matriz. Priorizar el protocolo de campo y la revisión conjunta de A06/A07. Preparar A09 en paralelo con los supuestos del piloto. Dirección conserva la decisión de aprobar alcance, arquitectura, piloto y oferta con evidencia por hito.

**Regla de cierre.** Calidad comprueba el resultado contra el criterio de cada fila y registra versión, método, resultado y aprobación. Los cambios de documentación técnica aportan evidencia de diseño. Las pruebas verificadas aportan evidencia de funcionamiento. Un riesgo aceptado conserva su estado y responsable.
