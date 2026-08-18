# Smart-Football-Scouting-Player-Similarity-Analysis
Motor de búsqueda y recomendación de futbolistas mediante algoritmos de aprendizaje no supervisado y Similaridad de Coseno.


# ⚽ Smart Football Scouting & Player Similarity Analysis

## 📌 Descripción del Proyecto
En la gestión deportiva moderna y la analítica de scouting (*Moneyball*), identificar sustitutos adecuados para jugadores clave o descubrir talentos subevaluados representa uno de los mayores desafíos estratégicos. 

Este proyecto implementa un motor de búsqueda e identificación de futbolistas basado en **Vector Space Modeling (VSM)** y la métrica de **Similaridad de Coseno**. A través de métricas avanzadas normalizadas por 90 minutos, el sistema evalúa la huella táctica y el perfil técnico de un jugador objetivo para devolver el **Top-N de futbolistas más similares** dentro de una base de datos.

---

## 🛠️ Arquitectura y Metodología Analítica

1. **Filtrado Mínimo de Exposición:** Filtro de representatividad estadística para evaluar únicamente a jugadores con $\ge 900$ minutos disputados en la temporada, mitigando el sesgo por muestras pequeñas.
2. **Estandarización de Variables (Z-Score):** Ajuste de escalas heterogéneas mediante `StandardScaler`, garantizando que métricas de bajo volumen tengan el mismo peso algorítmico que métricas de alto volumen (ej. pases progresivos).
3. **Cálculo de Similaridad de Coseno:** Evaluación de la dirección y proporción de los vectores métricos $n$-dimensionales para determinar la proximidad del perfil táctico sin verse distorsionado por la magnitud.
4. **Visualización Multidimensional:**
   - **Gráfico de Radar:** Comparación visual directa del jugador objetivo vs. su mejor match.
   - **Dashboard en Power BI:** Matriz de Generación de Peligro (xG vs xA) e interfaz interactiva para directores técnicos y scouts.


---

## 📊 Métricas de Rendimiento Evaluadas ($P_{90}$)

| Métrica | Campo | Descripción Táctica |
| :--- | :--- | :--- |
| **Expected Goals** | `xg_per90` | Calidad de las oportunidades de gol generadas por remate. |
| **Expected Assists** | `xa_per90` | Probabilidad de que sus pases clave se conviertan en asistencia. |
| **Key Passes** | `key_passes_per90` | Pases que derivan en un tiro a puerta de un compañero. |
| **Passes to Box** | `passes_into_penalty_area_per90` | Pases completados con éxito dentro del área rival. |
| **Progressive Passes** | `progressive_passes_per90` | Pases hacia adelante que avanzan el balón $\ge 10$ yardas. |
| **Progressive Carries** | `progressive_carries_per90` | Conducciones individuales que ganan terreno significativo. |
| **Successful Dribbles** | `dribbles_completed_per90` | Regates o duelos individuales ganados en mano a mano. |

---

## Desarrollado como parte del Portafolio de Analítica Deportiva y Ciencias de Datos.
