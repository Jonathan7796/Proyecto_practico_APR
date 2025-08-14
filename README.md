# Proyecto_practico_APR
Repositorio generado para realizar el proyecto correspondiente a la materia de Aprendizaje por refuerzo, como parte del Máster en IA de la VIU.

## Integrantes
- Camilo José Alape Herrera
- Jonathan Catota

## Estructura
- `Proyecto_práctico_CA.ipynb`: Notebook principal donde se desarrolla el agente.
- `requirements.txt`: Dependencias necesarias (para entorno local si se desea).

## Requisitos
- Google Colab (recomendado por GPU).
- Python 3.10+
- Entorno `gym[atari]`, `torch`, `matplotlib`, `numpy`.

## Instrucciones
1. Ejecutar el notebook desde Google Colab.
2. Entrenar el agente y guardar los pesos.
3. Documentar resultados y justificar comportamiento final.

## Evaluación
- Requisito mínimo: media de recompensa > 20 en modo test.

# Proyecto Práctico — Aprendizaje por Refuerzo con DQN y Memory Replay

Este repositorio implementa distintas variantes de **Deep Q-Network (DQN)** aplicadas al entorno **SpaceInvaders** de Atari. El objetivo es comparar mejoras arquitectónicas y de entrenamiento, evaluando su impacto en la recompensa media.

## 📂 Estructura del proyecto

- **Parte 1:** Configuración del entorno y requisitos previos.
- **Parte 2:** Implementación de DQN con `keras-rl2`, incluyendo:
  - Double DQN
  - Dueling Networks
  - Ajustes de hiperparámetros (learning rate, gamma, target update, etc.)
- **Parte 3 (Sección 3.1):** Baseline con `Stable-Baselines3`:
  - `VecFrameStack` y wrappers estándar para Atari.
  - Checkpoints automáticos cada 50k pasos.
  - Evaluación periódica cada 25k pasos.
  - Gráficas de recompensa por episodio y media móvil.
- **Parte 4:** Comparativa de resultados y conclusiones.

## 🚀 Ejecución

1. Clonar el repositorio y abrir el notebook en Google Colab o entorno local.
2. Seguir las celdas de instalación y configuración.
3. Para reanudar desde checkpoints:
   - Asegurarse de que las rutas (`CKPT_DIR`, `BEST_DIR`) contengan los modelos guardados.
   - Ejecutar hasta la celda que carga el modelo (incluida).
4. Ejecutar la sección de evaluación y gráficas.

## 📊 Resultados clave

- Las versiones personalizadas alcanzaron recompensas pico más altas pero con variabilidad.
- El baseline SB3 mostró mayor estabilidad y reproducibilidad, ideal para comparativas.
- El mejor modelo superó consistentemente el umbral de recompensa media objetivo.

## 📌 Dependencias principales

- `tensorflow` y `keras` (para `keras-rl2`)
- `stable-baselines3`
- `gymnasium` + `ALE-py`
- `matplotlib` y `pandas` para análisis

## 📝 Notas

- Se recomienda usar Google Colab con GPU activada.
- El entrenamiento completo puede requerir varias horas.
- Los modelos y logs deben guardarse en Google Drive para evitar pérdida de progreso.

## 📄 Licencia

Este proyecto se distribuye bajo la licencia MIT.