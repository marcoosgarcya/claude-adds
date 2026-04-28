# CognitoStudy — Roadmap de Implementación
**Horizonte:** 12 semanas (3 meses) | **Presupuesto:** 50–200€/mes

---

## Visión General

```
SEMANA 1-2      SEMANA 3-4      SEMANA 5-8      SEMANA 9-12
│               │               │               │
FUNDACIÓN  →  LANZAMIENTO  →  OPTIMIZACIÓN  →  ESCALA
│               │               │               │
Tracking        Campaña 1       Matar perdedor  TikTok Ads
Creativos       Meta Ads live   Escalar ganador Retargeting
Landing         Monitoreo       Retargeting     Multi-plataforma
```

---

## FASE 1: Fundación (Semanas 1–2)

### Objetivo: Todo listo antes de gastar un euro

**Tracking (Semana 1 — BLOQUEANTE):**
- [ ] Meta Pixel instalado y verificado en cognitostudies.com
- [ ] Eventos: ViewContent, Lead, CompleteRegistration disparando correctamente
- [ ] GA4 instalado con evento `sign_up`
- [ ] UTM naming convention definida y documentada
- [ ] Dashboard de seguimiento creado en Google Sheets

**Creativos (Semana 1-2):**
- [ ] Grabar Video 1: "La Transformación" (prioridad máxima)
- [ ] Grabar Video 3: "Para opositores"
- [ ] Exportar en formato 9:16 (Reels/TikTok) Y 4:5 (Feed)
- [ ] Crear Carousel "5 cosas que hace CognitoStudy"

**Cuenta Meta Ads (Semana 1):**
- [ ] Meta Business Manager creado y verificado
- [ ] Método de pago añadido
- [ ] Pixel vinculado a la cuenta publicitaria
- [ ] Dominio cognitostudies.com verificado en Meta

**Landing Page Check (Semana 2):**
- [ ] La página de destino carga en < 3 segundos en móvil
- [ ] El botón CTA es visible sin hacer scroll en móvil
- [ ] El proceso de registro tiene ≤ 2 pasos
- [ ] Existe un mensaje de confirmación post-registro
- [ ] La página funciona en Safari iOS (mayor % del tráfico móvil)

---

## FASE 2: Lanzamiento (Semanas 3–4)

### Objetivo: Datos reales, no suposiciones

**Día 1 del lanzamiento:**
- [ ] Campaña 1 activa: 2 Ad Sets × 2 anuncios cada uno
- [ ] Presupuesto diario: 3–5€/día (no más)
- [ ] Objetivo de campaña: Conversiones → CompleteRegistration
- [ ] Si no tienes suficientes conversiones iniciales: usar Traffic primero, luego cambiar

**Primeros 7 días — Monitoreo diario:**

| Día | Qué revisar | Umbral de alarma |
|-----|-------------|-----------------|
| 1–3 | Pixel disparando, anuncios en estado "Activo" | Si está en "En revisión" >24h, contactar soporte |
| 3–5 | CTR por anuncio | < 0.8% = pausa ese anuncio |
| 5–7 | Primeras conversiones (aunque sean pocas) | 0 conversiones con >50 clics = revisar landing/tracking |

**Semana 4:**
- [ ] Comparar CPR entre Ad Sets
- [ ] El Ad Set con peor CPR (>3× del mejor): pausar
- [ ] Crear 1 nuevo anuncio con el hook ganador pero diferente cuerpo

---

## FASE 3: Optimización (Semanas 5–8)

### Objetivo: Bajar CPR, encontrar la audiencia ganadora

**Semana 5:**
- [ ] Análisis completo de los primeros 30 días:
  - ¿Qué anuncio tiene el CTR más alto?
  - ¿Qué audiencia tiene el CPR más bajo?
  - ¿Cuál es la tasa de activación post-registro?
- [ ] Pausar todo lo que tenga CPR > 3× el mejor
- [ ] Subir presupuesto un 20% al Ad Set ganador

**Semana 6:**
- [ ] Lanzar Campaña 2: Retargeting (si tienes >500 visitantes/mes)
- [ ] Presupuesto retargeting: 25% del total mensual
- [ ] Crear 2 anuncios nuevos de retargeting con mensajes diferentes

**Semana 7–8:**
- [ ] Testear 1 nuevo ángulo creativo (ej: comparación con competidor)
- [ ] A/B test de landing page: ¿CTA "Pruébalo gratis" vs "Empieza gratis hoy"?
- [ ] Revisar tasa de activación: ¿Cuántos registros se convierten en usuarios activos?

---

## FASE 4: Escala y Multi-plataforma (Semanas 9–12)

### Objetivo: Segundo canal + escalar ganadores

**Semana 9:**
- [ ] Evaluar resultados de Meta: ¿CPR < 3€? ¿Usuarios activos creciendo?
- [ ] Si Meta funciona → lanzar TikTok Spark Ads con los 2 mejores orgánicos
- [ ] Si Meta no funciona → investigar el problema antes de añadir plataformas

**TikTok Spark Ads (Semana 9–10):**
- [ ] Cuenta TikTok Ads Manager creada
- [ ] TikTok Pixel instalado y verificado
- [ ] Seleccionar 2-3 posts orgánicos con mejor tasa de retención de video
- [ ] Presupuesto inicial TikTok: 30–40€/mes
- [ ] Objetivo: Video Views primero, luego Traffic, luego Conversiones

**Semana 11–12:**
- [ ] Revisión completa de los 3 meses:
  - CAC total (todos los canales)
  - MAU alcanzados vs objetivo (100–500)
  - Retención D7 y D30
  - ¿Qué canal tiene el CAC más bajo?
- [ ] Decisión: ¿Mantener mismo presupuesto? ¿Reinvertir? ¿Buscar financiación?

---

## Checklist de Revisión Semanal (Lunes, 15 min)

```
□ Abrir Meta Ads Manager
□ Revisar gasto total de la semana
□ Ver CPR por anuncio → pausar los que superan 3× objetivo
□ Ver CTR por anuncio → anotar el mejor
□ Ver frecuencia → si >3.0, expandir audiencia o rotar creativo
□ Abrir GA4 → ver registros de la semana y tasa de activación
□ Actualizar Google Sheets con datos de la semana
□ Decidir: ¿cambio algo esta semana o dejo correr?
```

---

## Decisión en el Mes 3: ¿Qué sigue?

| Resultado | Situación | Acción |
|-----------|-----------|--------|
| CPR < 2€ + MAU creciendo | Funciona | Escalar presupuesto con cuidado (+20%/semana) |
| CPR 2–5€ + MAU plano | Validado pero ineficiente | Optimizar landing page y activación |
| CPR > 8€ o 0 conversiones | No funciona aún | Revisar producto-mercado fit antes de más inversión |
| Retención D7 < 20% | Problema de producto | Pausar ads, mejorar onboarding primero |

> **Regla fundamental:** Los ads no arreglan un problema de producto. Si los usuarios se registran pero no vuelven, el problema está en la app, no en los anuncios. Soluciona la retención antes de escalar la adquisición.
