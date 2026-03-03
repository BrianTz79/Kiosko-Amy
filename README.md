# 🤖 Kiosko AMY (Asistente Multimodal Autónomo)

![Estado](https://img.shields.io/badge/Estado-En_Desarrollo-yellow)
![Arquitectura](https://img.shields.io/badge/Arquitectura-Fog_Computing-blue)
![Hardware](https://img.shields.io/badge/Hardware-Raspberry_Pi_5_%7C_AMD_Ryzen-green)

## 📖 Sobre el Proyecto

**AMY** es un Kiosco Universitario Inteligente diseñado para ofrecer asistencia interactiva y accesible a los estudiantes. Utiliza Inteligencia Artificial Generativa y una arquitectura de *Fog Computing* para operar de manera autónoma, procesando voz a texto (ASR), razonamiento con modelos de lenguaje (LLMs) y síntesis de voz (TTS) en tiempo real.

El proyecto se centra en la **accesibilidad universal**, permitiendo la interacción mediante voz (para personas con discapacidad visual) y apoyos gráficos/subtítulos (para personas con discapacidad auditiva), eliminando la dependencia a la conectividad web pública.

## 🏗️ Arquitectura del Sistema

El proyecto se divide en dos nodos principales que se comunican a través de una API en la red local:

1. **Edge (Cliente - Raspberry Pi 5):** Interfaz física. Gestiona la pantalla táctil, captura de micrófono, altavoces y el botón físico de activación (Push-to-Talk).

2. **Servidor Local (Inferencia - Servidor Ubuntu):** Cerebro del sistema. Ejecuta microservicios Dockerizados para el procesamiento neuronal pesado, integrando un pipeline RAG (Retrieval-Augmented Generation) con información institucional.

## 📂 Estructura del Repositorio

```text
Kiosko-Amy/
├── client/      # Interfaz gráfica y control de hardware (Raspberry Pi)
├── server/      # Servicios Docker, API REST/WebSockets y RAG pipeline
├── docs/        # Documentación técnica, diagramas y notas MD
├── scripts/     # Herramientas de despliegue y testeo
└── README.md    # Este archivo
