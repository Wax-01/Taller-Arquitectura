# 🗒️ Registro de Trabajo en Clase - Taller 3: Arquitectura Actual del Sistema con el Modelo C4

## 📆 Fecha de la sesión
Sábado 05/09/2026

## 👥 Integrantes presentes
- Julian David Aguilar
- Juan Esteban Ramirez

## 🧠 Actividades realizadas en clase

- Se revisó la [guía paso a paso del Taller 3](guia_paso_a_paso_c4.md) y su leyenda de notación para C1 y C2, y se acordó seguir la metodología de 4 pasos por vista antes de tocar draw.io.
- Se modeló el caso base de **RedExpress** siguiendo la metodología:
  - **C1**: se listaron primero los tres actores del enunciado (Usuario Final, Mensajero, Operador Logístico), se dibujó la Plataforma RedExpress como una sola caja (sin desglosar módulos) y se identificaron los dos sistemas externos (API de Notificaciones, Proveedor de Geolocalización). Se discutió si Power BI-like dashboards internos deberían aparecer aquí — se descartó porque ese nivel de detalle pertenece al C2.
  - **C2**: se descompuso la Plataforma RedExpress en sus 6 contenedores (App Móvil, Portal Web Operadores, Módulo de Gestión de Paquetes, Motor de Rutas, Seguimiento GPS, Sistema de Alertas) y se ubicó la infraestructura de soporte (Balanceador de Carga, Base de Datos Distribuida).
- Se discutió con el equipo qué protocolo asignar a cada relación (REST vs WebSocket) para el Seguimiento GPS, ya que la actualización de ubicación debe ser cercana a tiempo real; se decidió modelarla como `Push/WebSocket` desde Seguimiento GPS hacia la App Móvil.
- Se validaron ambos diagramas contra la [checklist de autoevaluación](guia_paso_a_paso_c4.md#checklist-de-autoevaluación-antes-de-entregar): ningún actor ni sistema externo quedó sin conexión, y cada contenedor quedó con tecnología/tipo indicado.
- Herramienta usada: **draw.io** (archivos `.drawio` adjuntos en esta carpeta).

## 🧩 Boceto inicial del modelo

Los bocetos finales de la sesión de clase quedaron guardados como:
- [`c1-contexto-borrador.drawio`](c1-contexto-borrador.drawio)
- [`c2-contenedores-borrador.drawio`](c2-contenedores-borrador.drawio)

Ambos siguen paso a paso el ejemplo guiado de RedExpress de la [guía](guia_paso_a_paso_c4.md#a3-ejemplo-guiado-contexto-de-redexpress), con la notación de color de la leyenda (persona = azul, sistema en alcance = azul oscuro, sistema externo = gris de doble borde, contenedor = azul claro, infraestructura = gris).

## 🔁 Tareas definidas para complementar el taller

| Tarea asignada | Responsable | Fecha estimada |
|----------------|-------------|----------------|
| Levantar información del cliente real (Universidad de La Sabana) reutilizando hallazgos de Taller 0 (ficha de caracterización), Taller 1 (BPMN) y Taller 2 (modelo de información) | Julian David Aguilar | 08/09 |
| Modelado C1 y C2 finales del cliente real en draw.io (`entrega/`) | Juan Esteban Ramirez | 10/09 |
| Redacción del informe técnico (`entrega/informe.md`) y referencias (`entrega/referencias.md`) | Julian David Aguilar | 12/09 |

---

_Este documento resume el trabajo colaborativo realizado durante la sesión del Taller 3 en el curso AREM - Universidad de La Sabana._
