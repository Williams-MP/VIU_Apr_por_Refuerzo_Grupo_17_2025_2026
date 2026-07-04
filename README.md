# VIU_Apr_por_Refuerzo_Grupo_17_2025_2026
Repositorio para la entrega del proyecto de programación grupo 17


# Aprendizaje por Refuerzo Profundo aplicado a Atari Enduro

**Grupo 17 · Curso 2025–2026 · Máster en Inteligencia Artificial (MIAR)**

Este repositorio contiene el desarrollo, entrenamiento y evaluación comparativa de distintas variantes del algoritmo **Deep Q-Network (DQN)** aplicadas al entorno **Enduro-v0** de Atari, implementadas con `keras-rl2` sobre TensorFlow/Keras y ejecutadas en Google Colab.

## Descripción

El objetivo del proyecto es analizar cómo las principales mejoras propuestas sobre el DQN original afectan al rendimiento del agente en un entorno de conducción de dificultad no trivial. Para ello se diseñan y comparan **ocho propuestas (P1–P8)** que combinan de forma incremental las siguientes técnicas:

- **DQN** (Q-learning profundo con experience replay y red objetivo)
- **Double DQN** — reduce la sobreestimación de los valores Q
- **Dueling DQN** — separa la estimación del valor de estado y la ventaja de cada acción
- Ajustes en la política de exploración (annealing de epsilon) y demás hiperparámetros

## Entorno

- **Juego:** Enduro-v0 (Atari 2600)
- **Preprocesado:** conversión a escala de grises, redimensionado y apilado de frames
- **Framework de RL:** `keras-rl2`
- **Backend:** TensorFlow / Keras
- **Ejecución:** Google Colab (GPU)


## Metodología

El notebook está organizado de forma modular en torno a un registro central de agentes (`AGENTS_REGISTRY`), con funciones reutilizables para construir, entrenar, cargar y evaluar cada propuesta de manera independiente y reproducible. Se incluye además una celda de análisis diagnóstico que genera tablas resumen, curvas de recompensa suavizada y diagnósticos por propuesta a partir de los resultados almacenados.

## Resultados

La propuesta **P5 (Dueling DQN)** obtuvo cumplió el requisitio de superar el primer día de carrera en 100 episodios consecutivos. 1 día de carrera equivale a obtener 200 puntos. Se obtiene 1 punto por cada coche adelantado.

## Referencias

- Mnih et al. (2013). *Playing Atari with Deep Reinforcement Learning.*
- Mnih et al. (2015). *Human-level control through deep reinforcement learning.*
- Van Hasselt et al. (2016). *Deep Reinforcement Learning with Double Q-learning.*
- Wang et al. (2016). *Dueling Network Architectures for Deep Reinforcement Learning.*

## Autores

Grupo 17 — Angel, Maria, Marina y Williams
