# SnackCheck - Automatización de Análisis Nutricional en n8n

SnackCheck es un flujo de trabajo automatizado desarrollado en n8n que permite consultar el perfil nutricional de productos alimenticios mediante su código de barras y generar un veredicto de salud claro mediante Inteligencia Artificial (LLM).

---

## Arquitectura del Flujo

El flujo sigue las siguientes etapas secuenciales de procesamiento:

1. Recepción Webhook: Escucha peticiones POST con un código de barras.
2. Validación de Entrada: Verifica que el código de barras esté presente y sea un valor puramente numérico.
3. Consulta API (Open Food Facts): Consulta los datos del producto en la base de datos pública.
4. Validación Nutricional: Asegura que el producto exista y cuente con información nutricional procesable.
5. Evaluación con IA (LLM): Procesa y aplana la información para generar un análisis simplificado y veredicto de salud.
6. Respuesta HTTP: Devuelve la respuesta correspondiente al cliente.

---

## Respuestas y Manejo de Errores

El flujo maneja respuestas estandarizadas según el resultado del procesamiento:

* HTTP 200 (OK): Producto encontrado y veredicto de IA generado correctamente.
* HTTP 400 (Bad Request): Código de barras no proporcionado o con caracteres no numéricos.
* HTTP 404 (Not Found): Código de barras no localizado en la base de datos.
* HTTP 422 (Unprocessable Entity): Producto localizado pero carece de datos nutricionales suficientes.

---

## Requisitos de Instalación

1. Tener una instancia activa de n8n.
2. Credenciales configuradas para el servicio de IA (LLM / OpenAI / Anthropic).
3. Importar el archivo workflow.json adjunto en tu canvas de n8n.

---

## Estructura de Entregables del Proyecto

* workflow.json: Exportación del flujo funcional en n8n.
* diagrama_excalidraw.png: Diagrama visual de decisiones y rutas del flujo.
* README.md: Documentación técnica e instrucciones del proyecto.
* TEST_CASES.md: Registro de casos de prueba y respuestas HTTP.
* CHANGELOG.md: Registro de versiones (SemVer v1.0.0).
