# Diagramas del Curso de Supervivencia

Este archivo contiene todos los diagramas Mermaid del curso para su uso en presentaciones y materiales complementarios.

---

## Diagrama 1: Regla de los Tres (Prioridades de Supervivencia)

```mermaid
flowchart TD
    subgraph REGLA["⏱️ REGLA DE LOS TRES"]
        A["🌬️ 3 MINUTOS<br/>sin aire"] --> B["❄️ 3 HORAS<br/>sin refugio (clima extremo)"]
        B --> C["💧 3 DÍAS<br/>sin agua"]
        C --> D["🍖 3 SEMANAS<br/>sin comida"]
    end

    style A fill:#ff6b6b,color:#fff
    style B fill:#ffa502,color:#fff
    style C fill:#3498db,color:#fff
    style D fill:#2ecc71,color:#fff
```

---

## Diagrama 2: Ciclo OODA (Toma de Decisiones)

```mermaid
flowchart LR
    O1[("👁️ OBSERVAR<br/>Evaluar situación")] --> O2[("🧠 ORIENTAR<br/>Analizar datos")]
    O2 --> D[("📋 DECIDIR<br/>Elegir acción")]
    D --> A[("⚡ ACTUAR<br/>Ejecutar")]
    A -.->|"Feedback"| O1

    style O1 fill:#3498db,color:#fff
    style O2 fill:#9b59b6,color:#fff
    style D fill:#e67e22,color:#fff
    style A fill:#2ecc71,color:#fff
```

---

## Diagrama 3: Métodos de Encendido de Fuego

```mermaid
flowchart TD
    FUEGO["🔥 MÉTODOS DE FUEGO"]

    FUEGO --> FRICCION["⚙️ FRICCIÓN"]
    FUEGO --> CHISPA["✨ CHISPA"]
    FUEGO --> SOLAR["☀️ SOLAR"]

    FRICCION --> ArcoFuego["Arco de fuego<br/>⭐⭐⭐"]
    FRICCION --> HandDrill["Hand Drill<br/>⭐⭐⭐⭐⭐"]
    FRICCION --> Arado["Arado de fuego<br/>⭐⭐⭐⭐"]

    CHISPA --> Ferrocerio["Ferrocerio<br/>⭐"]
    CHISPA --> Pedernal["Pedernal + Eslabon<br/>⭐⭐"]
    CHISPA --> Encendedor["Encendedor BIC<br/>⭐"]

    SOLAR --> Lupa["Lupa/Lente<br/>⭐⭐"]
    SOLAR --> Espejo["Espejo parabolico<br/>⭐⭐⭐"]

    style FUEGO fill:#ff6b35,color:#fff
    style FRICCION fill:#e74c3c,color:#fff
    style CHISPA fill:#f39c12,color:#fff
    style SOLAR fill:#f1c40f,color:#000
```

---

## Diagrama 4: Árbol de Decisión para Refugio

```mermaid
flowchart TD
    START["🏕️ ¿NECESITAS REFUGIO?"]

    START --> CLIMA{"¿Clima principal?"}

    CLIMA -->|Lluvia| LLUVIA["Prioridad: Impermeabilidad"]
    CLIMA -->|Frío| FRIO["Prioridad: Aislamiento"]
    CLIMA -->|Calor| CALOR["Prioridad: Sombra"]
    CLIMA -->|Viento| VIENTO["Prioridad: Cortavientos"]

    LLUVIA --> LEANTO["LEAN-TO<br/>Inclinado 45°"]
    FRIO --> DEBRIS["DEBRIS HUT<br/>Enterrado en hojarasca"]
    CALOR --> SOMBRA["TOLDO ELEVADO<br/>Circulación de aire"]
    VIENTO --> MURO["MURO + CUEVA<br/>Piedras apiladas"]

    style START fill:#2ecc71,color:#fff
    style CLIMA fill:#3498db,color:#fff
    style LLUVIA fill:#9b59b6,color:#fff
    style FRIO fill:#1abc9c,color:#fff
    style CALOR fill:#e67e22,color:#fff
    style VIENTO fill:#34495e,color:#fff
```

---

## Diagrama 5: Proceso de Purificación de Agua

```mermaid
flowchart LR
    subgraph FUENTE["📍 FUENTE"]
        A1["Río/Arroyo"]
        A2["Lago"]
        A3["Charco"]
        A4["Lluvia"]
    end

    subgraph FILTRADO["🔬 FILTRADO"]
        B1["Tela/Arena<br/>Partículas"]
        B2["Filtro comercial<br/>Bacterias"]
    end

    subgraph PURIFICACION["🧪 PURIFICACIÓN"]
        C1["Hervido<br/>1-10 min"]
        C2["Químico<br/>Yodo/Cloro"]
        C3["UV<br/>Solar/SteriPEN"]
    end

    subgraph SEGURA["✅ SEGURA"]
        D["💧 Agua potable"]
    end

    A1 & A2 & A3 --> B1
    B1 --> B2
    A4 --> B1
    B2 --> C1 & C2 & C3
    C1 & C2 & C3 --> D

    style D fill:#2ecc71,color:#fff
```

---

## Diagrama 6: Evolución Histórica de Habilidades

```mermaid
timeline
    title Evolución de Habilidades de Supervivencia

    section Paleolítico
        2.5M - 10000 AC : Fuego por fricción
                       : Refugios naturales
                       : Caza/Recolección

    section Neolítico
        10000 - 3000 AC : Herramientas líticas
                       : Agricultura básica
                       : Preservación alimentos
                       : Cordaje/Cestería

    section Edad Metales
        3000 AC - 500 DC : Metalurgia campo
                        : Trampas avanzadas
                        : Navegación terrestre

    section Medieval
        500 - 1500 DC : Navegación celeste
                     : Medicina herbal
                     : Defensa campamento

    section Industrial
        1750 - 1950 : Primeros auxilios
                   : Señalización rescate
                   : Mecánica emergencia

    section Moderna
        1950 - Presente : Supervivencia urbana
                       : Comunicaciones
                       : Preparacionismo
```

---

## Diagrama 7: Protocolo ABC de Emergencias Médicas

```mermaid
flowchart TD
    START["🚨 EMERGENCIA MÉDICA"]

    START --> SEGURO{"¿Escena segura?"}
    SEGURO -->|No| ALEJAR["Alejar peligro o<br/>mover víctima"]
    SEGURO -->|Sí| A
    ALEJAR --> A

    A["A - AIRWAY<br/>¿Vía aérea permeable?"]
    A -->|No| MANIOBRA["Maniobra frente-mentón"]
    A -->|Sí| B
    MANIOBRA --> B

    B["B - BREATHING<br/>¿Respira? (VOS)"]
    B -->|No| RCP["Iniciar RCP<br/>30:2"]
    B -->|Sí| C

    C["C - CIRCULATION<br/>¿Pulso? ¿Hemorragia?"]
    C -->|Hemorragia| CONTROL["Presión directa<br/>Elevación<br/>Torniquete"]
    C -->|Sin pulso| RCP
    C -->|Estable| MONITOR["Monitorizar<br/>Posición lateral"]

    style START fill:#e74c3c,color:#fff
    style A fill:#3498db,color:#fff
    style B fill:#2ecc71,color:#fff
    style C fill:#9b59b6,color:#fff
    style RCP fill:#e74c3c,color:#fff
```

---

## Diagrama 8: Señales Internacionales de Tierra-Aire

```mermaid
flowchart LR
    subgraph SEÑALES["✈️ SEÑALES TIERRA-AIRE"]
        V["V<br/>NECESITO AYUDA"]
        X["X<br/>ATENCIÓN MÉDICA"]
        I["I<br/>VOY EN ESTA DIRECCIÓN"]
        FLECHA["→<br/>SÍGANME"]
        LL["LL<br/>TODO BIEN"]
    end

    subgraph CUERPO["🧍 SEÑALES CON CUERPO"]
        AYUDA["Y<br/>Brazos arriba = AYUDA"]
        BIEN["/<br/>Un brazo arriba = OK"]
    end

    style V fill:#e74c3c,color:#fff
    style X fill:#e74c3c,color:#fff
    style AYUDA fill:#f39c12,color:#fff
```

---

## Diagrama 9: Plan de Evacuación Urbana

```mermaid
flowchart TD
    ALERTA["⚠️ ALERTA DE EVACUACIÓN"]

    ALERTA --> EVALUAR{"¿Evacuar o quedarse?"}

    EVALUAR -->|"Peligro inmediato<br/>Orden oficial<br/>Sin recursos"| EVACUAR["🚗 EVACUAR"]
    EVALUAR -->|"Estructura segura<br/>Recursos OK<br/>Carreteras bloqueadas"| QUEDARSE["🏠 QUEDARSE"]

    EVACUAR --> BOB["Coger BOB<br/>(Bug Out Bag)"]
    BOB --> RUTA["Seguir ruta<br/>predeterminada"]
    RUTA --> DESTINO["Llegar a destino<br/>seguro"]

    QUEDARSE --> AISLARSE["Asegurar hogar"]
    AISLARSE --> RESERVAS["Usar reservas<br/>72h mínimo"]
    RESERVAS --> ESPERAR["Esperar ayuda<br/>o mejora"]

    style ALERTA fill:#e74c3c,color:#fff
    style EVACUAR fill:#3498db,color:#fff
    style QUEDARSE fill:#2ecc71,color:#fff
```

---

## Diagrama 10: Contenido del Bug Out Bag (BOB)

```mermaid
mindmap
  root((🎒 BOB<br/>72 Horas))
    💧 Agua
      Botella 1L acero
      Filtro LifeStraw
      Pastillas potabilizadoras
    🍖 Alimentación
      Barritas energéticas
      Frutos secos
      Comida liofilizada
    🏕️ Refugio
      Manta emergencia
      Poncho
      Paracord 15m
    🔥 Fuego
      Encendedor x2
      Ferrocerio
      Yesca preparada
    🩹 Primeros Auxilios
      Vendas/Gasas
      Antiséptico
      Medicación personal
    🔧 Herramientas
      Cuchillo fijo
      Multiherramienta
      Linterna frontal
    📄 Documentación
      Copias DNI
      Efectivo
      Mapa físico
    📻 Comunicación
      Radio AM/FM
      Cargador solar
```

---

## Prompts para Generación de Imágenes (DALL-E / Midjourney)

### Imagen 1: Portada del Curso
```
Survival course cover illustration, prehistoric to modern evolution theme, showing silhouettes of humans through ages (caveman with fire, medieval explorer with compass, modern prepper with backpack), warm earth tones gradient background, educational documentary style, cinematic lighting, 16:9 aspect ratio
```

### Imagen 2: Encendido de Fuego por Arco
```
Detailed instructional illustration of bow drill fire starting technique, hands demonstrating proper form, wooden spindle and fireboard, ember forming in notch, smoke rising, wilderness background, technical diagram style with clean lines, warm lighting, educational
```

### Imagen 3: Construcción de Refugio Debris Hut
```
Cross-section illustration of debris hut survival shelter construction, cutaway view showing internal structure with person inside, layers of leaves and branches visible, forest setting, technical educational style, labeled diagram aesthetic, natural colors
```

### Imagen 4: Navegación por Estrellas
```
Educational night sky illustration showing Big Dipper (Osa Mayor) pointing to Polaris (North Star), dotted lines connecting stars, constellation labels, dark blue starry background, vintage astronomy chart style, educational infographic
```

### Imagen 5: Kit de Supervivencia Desplegado
```
Flat lay photography style illustration of complete survival kit contents arranged neatly on dark background, knife, fire starter, water filter, first aid, paracord, compass, emergency blanket, organized grid layout, product photography lighting, detailed realistic style
```

### Imagen 6: Planta Comestible vs Venenosa
```
Side by side botanical comparison illustration, edible wild plant on left (clearly marked safe), poisonous look-alike on right (marked danger), detailed leaf and berry drawings, field guide style, educational labels pointing to key differences, clean white background
```

---

## Notas de Uso

1. Los diagramas Mermaid pueden renderizarse en:
   - GitHub/GitLab (nativamente)
   - Obsidian
   - VS Code con extensión Mermaid
   - mermaid.live (editor online)

2. Los prompts de imagen están optimizados para:
   - DALL-E 3
   - Midjourney v5+
   - Stable Diffusion XL

3. Para exportar diagramas a PNG/SVG, usar mermaid-cli o mermaid.live
