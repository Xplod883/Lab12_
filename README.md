# Lab12_
Creación de un Chatbot Inteligente en C++ vinculando Inteligencia Artificial a través de HTTP.

Objetivo
• Aplicar estrategias de búsqueda de patrones para construir un chatbot sencillo en C++.
• Utilizar servicios de inteligencia artificial como ChatGPT u otra IA para asistir en el diseño, codificación o depuración del chatbot.
• Aprender a consultar bases de conocimiento locales o externas.
• (Opcional) Integrar el uso de la API oficial de OpenAI.

Parte A: Chatbot Local Basado en Base de Conocimiento
Descripción General

Debes desarrollar un chatbot que:
1. Lea un archivo de base de datos local (conocimiento.txt) donde cada línea contiene una pregunta|respuesta.
2. Permita al usuario escribir preguntas por consola.
3. Busque respuestas usando algoritmos de:
  o Búsqueda exacta,
  o Búsqueda por palabras clave,
  o (Opcional) Similaridad de frases (por número de palabras comunes, distancia de Levenshtein, etc.).
4. Devuelva la respuesta encontrada o un mensaje adecuado si no encuentra coincidencia.

Requerimientos Específicos
• Usar std::map, std::vector o estructuras de datos similares para manejar la base de conocimiento.
• Implementar dos estrategias mínimas de búsqueda:
  o Exacta: Coincidencia 100% con la pregunta.
  o Palabras clave: Detectar palabras clave contenidas en preguntas del archivo.
• (Opcional) Mejorar la búsqueda usando métodos de similaridad básica.
• Imprimir en consola tanto la pregunta del usuario como la respuesta del chatbot.
• Manejar el caso cuando no haya respuesta adecuada.
Formato del Archivo conocimiento.txt

Ejemplo:
¿Cómo estás?|Estoy muy bien, gracias por preguntar.
¿Qué es un algoritmo?|Un algoritmo es una secuencia de pasos para resolver un
problema.
¿Quién inventó C++?|Bjarne Stroustrup creó el lenguaje C++.

Parte B: Uso Obligatorio de Inteligencia Artificial

Instrucción Especial

Debes utilizar ChatGPT, DeepSeek, GitHub Copilot u otra IA de programación para al menos UNA de las siguientes tareas:
• Generar ejemplos de código (por ejemplo: función para cargar archivo o buscar coincidencias).
• Depurar errores que surjan durante la programación.
• Optimizar fragmentos de código.
• Proponer algoritmos de búsqueda de patrones.

Debes documentar en un pequeño archivo informe.txt:
• ¿Qué preguntas hiciste a la IA?
• ¿Qué fragmentos de código o ideas generaste con ayuda de la IA?
• ¿Qué aprendiste al usarla?

Parte C (Opcional para Extra Puntos): Integración con API de OpenAI
Conectar tu chatbot a la API de OpenAI para enviar preguntas en vivo y recibir respuestas de un modelo como gpt-3.5-turbo.

Consideraciones:
• Usar librería libcurl o ejecutar llamadas HTTP externas.
• Necesitarás una cuenta gratuita en OpenAI y una API Key. Sugerencias Técnicas para la Integración
• Realizar una petición HTTP POST al endpoint: bash
https://api.openai.com/v1/chat/completions
• Enviar un cuerpo en formato JSON similar a:

json
{
  "model": "gpt-3.5-turbo",
  "messages": [{"role": "user", "content": "¿Qué es un algoritmo?"}]
}
• Incluir un Authorization: Bearer {API_KEY} en el encabezado.
