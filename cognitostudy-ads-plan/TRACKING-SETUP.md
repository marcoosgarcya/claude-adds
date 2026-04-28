# CognitoStudy — Checklist de Tracking
**⚠️ Configurar ANTES de gastar el primer euro en ads**

---

## Por qué el tracking es crítico con presupuesto ajustado

Con 100€/mes no puedes permitirte el lujo de no saber qué funciona. Cada euro debe ser trazable. Sin tracking correcto, estás volando a ciegas.

---

## Meta Pixel — Configuración Mínima Viable

### Instalación:
- [ ] Crear cuenta Meta Business Manager (business.facebook.com)
- [ ] Crear Pixel de Meta en Events Manager
- [ ] Instalar el código base en cognitostudies.com (todas las páginas)
- [ ] Verificar con Meta Pixel Helper (extensión Chrome)

### Eventos a configurar (en orden de prioridad):

| Evento | Trigger | Prioridad |
|--------|---------|-----------|
| `PageView` | Todas las páginas | P1 — incluido automáticamente |
| `ViewContent` | Página de inicio / features | P1 |
| `Lead` | Clic en botón "Registrarse" / inicio de formulario | P1 |
| `CompleteRegistration` | Registro completado exitosamente | P1 |
| `Subscribe` | Si implementas plan de pago | P2 |
| `Purchase` | Primer pago procesado | P2 |

### Verificación:
- [ ] Test Events en Meta Events Manager muestra eventos disparando
- [ ] Instalar Meta Pixel Helper y verificar en cognitostudies.com
- [ ] Configurar ventana de conversión: 7 días clic / 1 día view

---

## TikTok Pixel — Configuración (antes de lanzar TikTok Ads)

- [ ] Crear cuenta TikTok Ads Manager
- [ ] Instalar TikTok Pixel en cognitostudies.com
- [ ] Configurar eventos: ViewContent, CompleteRegistration
- [ ] Verificar con TikTok Pixel Helper

---

## Google Analytics 4 — Imprescindible (aunque no uses Google Ads)

- [ ] Instalar GA4 en cognitostudies.com
- [ ] Configurar eventos de conversión:
  - `sign_up`: registro completado
  - `login`: sesión iniciada (proxy de usuario activo)
  - `generate_content`: uso del feature principal
- [ ] Conectar GA4 con Meta (si es posible vía GTM)
- [ ] Crear informes de retención en GA4 para medir D7 y D30

---

## UTM Parameters — Trazabilidad de Campañas

Usar siempre UTMs en las URLs de destino de los anuncios:

```
https://cognitostudies.com/registro
?utm_source=meta
&utm_medium=paid_social
&utm_campaign=validacion_creativos_q2
&utm_content=video_transformacion
&utm_term=estudiantes_18_24_es
```

### Nomenclatura UTM para CognitoStudy:

| Parámetro | Valores |
|-----------|---------|
| utm_source | meta, tiktok, google, organic |
| utm_medium | paid_social, paid_search, cpc, reels, story |
| utm_campaign | [nombre_campaña_corto] |
| utm_content | [nombre_creativo: video_transformacion, carousel_features, etc.] |
| utm_term | [audiencia: estudiantes_es, opositores, latam_18_24] |

---

## Dashboard de Seguimiento (Google Sheets)

Crea una hoja de cálculo semanal con estas columnas:

| Semana | Plataforma | Campaña | Creativo | Gasto € | Impresiones | Clics | CTR% | Registros | CPR€ | Activos | CAC€ |
|--------|-----------|---------|---------|---------|-------------|-------|------|-----------|------|---------|------|

Actualizar cada lunes con datos de la semana anterior.

---

## Señales de Alarma

| Si ves esto... | Qué significa | Acción |
|----------------|---------------|--------|
| Pixel no dispara eventos | Instalación incorrecta | Revisar código, usar GTM |
| CTR alto pero 0 registros | Landing page con fricción o tracking roto | Revisar embudo post-clic |
| CPR muy alto (>10€) | Creativo o audiencia incorrectos | Rotar creativo, cambiar audiencia |
| Frecuencia >3 sin conversiones | Audiencia saturada | Expandir audiencia o pausar |
| GA4 no registra sign_up | Evento de conversión mal configurado | Revisar implementación |
