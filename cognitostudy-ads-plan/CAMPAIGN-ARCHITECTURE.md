# CognitoStudy — Arquitectura de Campañas
**Plataforma principal:** Meta Ads | **Fase:** Validación

---

## Convención de Nombres

```
[Plataforma]_[Objetivo]_[Audiencia]_[Geo]_[Trimestre]

Ejemplos:
META_REG_Estudiantes18-24_ES_2026Q2
META_RET_WebVisitors_LATAM_2026Q2
TIK_REG_Estudiantes_ES-MX_2026Q3
```

---

## Estructura de Cuenta — Meta Ads

```
Cuenta CognitoStudy
│
├── CAMPAÑA 1: Validación de Creativos (Mes 1)
│   Objetivo: Traffic / Registration
│   Presupuesto: 60–70% del total mensual
│   Estrategia: CBO (Campaign Budget Optimization)
│   │
│   ├── Ad Set 1A: Estudiantes España (Broad)
│   │   Edad: 18–26 | Geo: España
│   │   Intereses: Universidad, Estudiar, Productividad
│   │   Dispositivos: Todos (priorizar móvil)
│   │   └── Anuncio 1: Demo video 30s "Transformación apuntes"
│   │   └── Anuncio 2: Hook de dolor "¿Sigues resumiendo a mano?"
│   │   └── Anuncio 3: Screen recording + texto "10 segundos"
│   │
│   ├── Ad Set 1B: Oposiciones y Certificaciones (España)
│   │   Edad: 22–32 | Geo: España
│   │   Intereses: Oposiciones, MIR, Abogacía, Funcionario
│   │   └── Anuncio 1: Video específico "Para opositores"
│   │   └── Anuncio 2: Carousel features para volumen de estudio
│   │
│   └── Ad Set 1C: LATAM Estudiantes (México + Argentina)
│       Edad: 18–27 | Geo: México, Argentina, Colombia
│       Intereses: Universidad, Productividad, Tecnología
│       └── Anuncio 1: Mismos creativos que 1A (testear)
│
├── CAMPAÑA 2: Retargeting (Mes 2+)
│   Objetivo: Conversiones (Registro completado)
│   Presupuesto: 20–25% del total mensual
│   Condición de activación: cuando tengas >1,000 visitantes/mes
│   │
│   ├── Ad Set 2A: Visitantes web últimos 7 días
│   │   Audiencia personalizada: cognitostudies.com visitantes
│   │   └── Anuncio: "¿Ya lo probaste? Es gratis para empezar"
│   │
│   └── Ad Set 2B: Registros incompletos (si tienes pixel + eventos)
│       Audiencia: Inició registro pero no completó
│       └── Anuncio: "Tu cuenta te está esperando"
│
└── CAMPAÑA 3: Testing (Mes 2–3)
    Objetivo: Experimentación
    Presupuesto: 10–15% del total mensual
    │
    ├── Ad Set 3A: Competidor - Quizlet alternativa
    │   Intereses: Quizlet users (si disponible)
    │   └── Anuncio: Comparativa directa
    │
    └── Ad Set 3B: Jóvenes profesionales (reskilling)
        Edad: 25–32 | Intereses: Certificaciones, LinkedIn Learning
        └── Anuncio: Ángulo profesional/carrera
```

---

## Estructura TikTok Ads (Mes 2–3)

```
Cuenta CognitoStudy — TikTok
│
├── CAMPAÑA 1: Spark Ads (amplificar orgánico)
│   Objetivo: Video Views / Traffic
│   Estrategia: Seleccionar los 2-3 posts orgánicos con mejor retención
│   Presupuesto: 30€/mes mínimo
│   │
│   └── Ad Set 1A: Broad Estudiantes 18-25
│       Geo: España + México + Argentina
│       Intereses: Education, Productivity, Technology
│       └── Spark del video orgánico con mejor tasa de completado
│
└── CAMPAÑA 2: In-Feed Ads (Mes 3+)
    Objetivo: Conversiones (registro)
    Presupuesto: cuando Spark Ads demuestren CTR >2%
    └── Ad Set 2A: Custom Audience (visitantes web vía Pixel TikTok)
```

---

## Audiencias Personalizadas a Construir

Desde el primer día, configura estas audiencias (no cuestan nada, solo acumulan datos):

| Audiencia | Fuente | Ventana | Uso |
|-----------|--------|---------|-----|
| Visitantes web | Pixel Meta | 30 días | Retargeting |
| Visitantes página de registro | Pixel Meta | 7 días | Alta intención |
| Visitantes web | Pixel TikTok | 30 días | Retargeting TikTok |
| Lista de emails | Upload manual | — | Lookalike seed |

### Lookalikes (activar en mes 2–3):
- Lookalike 1%: basado en visitantes web (mínimo 1,000 personas en audiencia source)
- Lookalike 1%: basado en lista de emails de usuarios registrados

---

## Segmentación de Intereses — Meta (Validados para EdTech España/LATAM)

**Tier 1 (mayor volumen y relevancia):**
- Educación universitaria
- Estudio y productividad
- Inteligencia artificial
- Aplicaciones de productividad

**Tier 2 (nichos específicos):**
- Oposiciones España
- Examen de selectividad / UNAM / PAU
- Certificaciones profesionales (PMP, CFA, IELTS)
- Notion, Quizlet (audiencias de competidores si disponible)

**Tier 3 (para lookalikes y broad):**
- Jóvenes 18-30 + Spain/Mexico/Argentina sin intereses específicos
- Testar Broad Targeting — Meta's IA suele funcionar bien con buen creativo

---

## Exclusiones Obligatorias

- Clientes ya registrados (lista de emails subida como Custom Audience)
- Usuarios que ya completaron registro (evento Pixel: Complete Registration)
- Menores de 18 años
