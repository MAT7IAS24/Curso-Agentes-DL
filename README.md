# Curso de Agentes de IA — Deep Learning

Repositorio de evidencias prácticas del [AI Agents Course de Hugging Face](https://huggingface.co/learn/agents-course).

**Estudiante:** Mattias Morales  
**Username de Hugging Face:** [MAT7IAS24](https://huggingface.co/MAT7IAS24)  
**Asignatura:** Deep Learning  
**Universidad:** Universidad Externado de Colombia  
**Profesor:** Alber Montenegro  
**Certificado obtenido:** Fundamentals of Agents (Unidad 1; fecha de emisión indicada: 6 de noviembre de 2026)

## Organización del repositorio

| Unidad | Notebook | Actividad |
| --- | --- | --- |
| Unidad 0 | `Unidad_0/Unidad_0_Configuracion_Gemini.ipynb` | Configuración de Gemini en Colab y primer agente de promedio |
| Unidad 1 | `Unidad_1/Unidad_1_Dummy_Agent.ipynb` | Ciclo de acción, herramienta y observación con clima simulado |
| Unidad 1 | `Unidad_1/Unidad_1_Alfred_smolagents.ipynb` | Agente Alfred para consultar una zona horaria |

## Requisitos de ejecución

- Python en Google Colab.
- Librería `smolagents` y cliente compatible con OpenAI.
- Una API key de Gemini almacenada de forma privada en Colab **Secrets**, bajo el nombre `GEMINI_API_KEY`.
- El modelo usado en las prácticas fue `gemini-3.5-flash-lite`; la disponibilidad y las cuotas pueden cambiar.

**Seguridad:** no se deben subir claves de API al repositorio ni escribirlas directamente en los notebooks.

## Prácticas y resultados

### Unidad 0: Configuración de Gemini

Se configuró la API de Gemini desde Google Colab. Tras obtener una respuesta sobre qué es un agente, se creó un `CodeAgent` que utilizó la herramienta `calcular_promedio`. El promedio de 8, 10, 15 y 19 fue **13.0**.

### Unidad 1: Dummy Agent Library

Se adaptó el ejemplo del tutorial oficial para usar Gemini en lugar de los servicios de inferencia de Hugging Face. El modelo generó la acción `get_weather` para Londres y el código ejecutó la función local. **El clima de la práctica es simulado; no es una consulta meteorológica real.**

### Unidad 1: Alfred con `smolagents`

Se implementó un agente con una herramienta Python que consulta la hora de una zona horaria IANA mediante `datetime` y `zoneinfo`. En la ejecución guardada, Alfred primero registró un error de interpretación, luego ejecutó correctamente la herramienta para `America/Bogota` y devolvió la hora obtenida.

La práctica se ejecutó en **Google Colab**; no se afirma que se haya publicado un Space en Hugging Face.

## Conclusiones

Las prácticas permiten distinguir entre una consulta directa a un LLM y un agente con herramientas. En el ejercicio manual se separaron la solicitud del modelo, la ejecución de una función y la observación, mientras que `smolagents` automatizó buena parte de ese flujo.

## Certificación y evidencias

Se obtuvo el certificado **Fundamentals of Agents** al aprobar el cuestionario final de la Unidad 1. Las capturas de progreso y el certificado se presentan por separado en el PDF de evidencias de la asignatura. El historial de commits debe reflejar las fechas reales de trabajo.
