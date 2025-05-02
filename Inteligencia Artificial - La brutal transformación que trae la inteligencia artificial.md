Por José Alvers Wiiber Francisco.

**Resumen de la Ponencia: "La Brutal Transformación que Trae la Inteligencia Artificial"**

La conferencia, impartida por Herbert Alvers (Economista y Arquitecto de TI Senior en IBM, actualmente liderando el equipo de Account Technical Leaders en IBM México), se centró en los conceptos y el impacto de la inteligencia artificial (IA), especialmente en el contexto de su evolución y su futuro marcado por el movimiento _open source_.

1. **Historia y Evolución de la IA:**
    - La IA es una disciplina que comenzó en los años 50 en el ámbito académico, específicamente en una reunión en la Universidad de Dartmouth. Próximamente se celebrarán 75 años de su existencia.
    - IBM ha estado involucrado en la IA desde sus inicios.
    - La definición de inteligencia artificial ha cambiado con el tiempo a medida que se han resuelto problemas que antes se consideraban exclusivos de la inteligencia humana, como el reconocimiento visual.
    - Hitos importantes en la historia de la IA incluyen la capacidad de jugar a las damas (resuelto en los 60), al ajedrez (Deep Blue de IBM ganó al campeón mundial Gary Kasparov a finales de los 90), ganar en Jeopardy (otra computadora de IBM), y el Proyecto Debater de IBM en 2018, que demostró la capacidad de debatir con un humano en tiempo real sobre temas complejos.

2. **Fundamentos de la IA:**
    - La IA es el término genérico, que incluye subconjuntos como el **Machine Learning (ML)** o aprendizaje automático, y el **Deep Learning (DL)** o aprendizaje profundo, que a menudo se refiere a tecnologías de redes neuronales.
    - Lo que define estos tipos son los algoritmos utilizados.
    - Los sistemas de IA, a diferencia de los humanos, no tienen sentido común, conocimiento del mundo o conciencia. Adquieren conocimiento a través de la experiencia (cognición), aprendiendo de los datos y la experiencia humana utilizando algoritmos.
    - **La disponibilidad de datos es fundamental** para el entrenamiento de los modelos de IA. La explosión de la IA en los últimos 25 años se debe en gran medida a la abundancia de datos, especialmente con el auge de Internet y la Web 2.0. Ejemplos incluyen la documentación histórica de partidas de ajedrez y bases de datos como ImageNet para el reconocimiento de imágenes.
    - Los algoritmos de IA **son probabilísticos**, no determinísticos. Esto significa que los resultados son predicciones con un grado de probabilidad, no certezas absolutas. Esta característica, aunque implica la posibilidad de errores (a menudo heredados de los datos de entrenamiento), es lo que ha permitido la expansión de la IA a muchos ámbitos. Es crucial que los usuarios verifiquen los resultados generados por los sistemas de IA, como los LLMs.

3. **Tipos de Aprendizaje Automático:**
    - **Aprendizaje Automático Clásico:** A menudo asociado a la ciencia de datos, se basa en algoritmos estadísticos bien conocidos (regresión lineal, árboles de decisión, etc.). Es muy utilizado en empresas porque trabaja bien con **datos estructurados** provenientes de bases de datos tradicionales. Se aplica para predecir demanda, riesgo de abandono de clientes (_churn_), o evaluar la concesión de créditos. Una característica importante es su **facilidad de explicación**, lo que permite entender por qué un sistema tomó una decisión y mitigar sesgos o discriminación.
    - **Aprendizaje Profundo (Deep Learning):** Popularizado desde los años 2000, utiliza **redes neuronales**, descritas como estructuras de datos con múltiples capas que procesan información. Han permitido resolver problemas complejos como el Reconocimiento Óptico de Caracteres (OCR), clave para digitalizar información para entrenar LLMs. Entrenar redes neuronales profundas (con millones de capas) requiere un cálculo matricial intensivo que demanda gran poder computacional (GPUs). Aunque potentes, **no funcionan como un cerebro humano** y carecen de características como la iniciativa o la curiosidad. El conocimiento aprendido se representa en la estructura numérica del modelo, no como una copia de los datos originales.

4. **IA Generativa y Modelos de Lenguaje Grandes (LLMs):**
    - La IA Generativa se basa en las redes neuronales y ha explotado en los últimos 5 años.
    - Los LLMs son modelos de lenguaje a gran escala (ahora también capaces de generar imágenes u otros datos) basados en redes neuronales (especialmente la arquitectura **Transformers**, basada en el paper de 2018 "All You Need Is Attention"). Están entrenados con enormes cantidades de datos para procesar y generar texto coherente y natural. Inicialmente funcionaban como autocompletadores inteligentes.
    - **Aplicaciones de los LLMs** incluyen asistentes virtuales y chatbots (usados en México por grandes empresas de telecomunicaciones y banca), análisis y resumen de textos, generación y depuración de código (requiere conocimiento para validar y corregir), y traducción de contenido (necesita revisión humana).
    - El ponente mencionó varios LLMs conocidos: Quen (Alibaba), DeepSeek, LLaMA (Facebook), Mistral (Francia), **IBM Granite** (Open Source), Claude (Anthropic), OpenAI (ChatGPT), Gemini (Google), Grok (Elon Musk), y Copilot (Microsoft).
    - 
5. **El Futuro Open Source de la IA:**
    - Un mensaje central es que **el futuro de la IA es _open source_**, no de tecnología propietaria. Se compara con el _middleware_, donde soluciones abiertas como PostgreSQL son competitivas y más accesibles que las propietarias.
    - IBM apoya la idea de múltiples modelos especializados, no uno solo que resuelva todo.
    - **Modelos más pequeños y especializados** son más eficientes, requieren menos energía, son más rápidos y pueden correr localmente, lo cual es preferido por las empresas para proteger su información y evitar compartirla.
    - Plataformas como **Hugging Face** permiten a la comunidad compartir y descargar modelos _open source_ (incluyendo los de IBM Granite).
    - La **innovación** en IA está impulsada por el mundo _open source_, las universidades y los institutos de investigación.
    - La diferencia de rendimiento entre modelos comerciales y _open source_ se está reduciendo rápidamente. Incluso empresas grandes como Google han reconocido la fortaleza del movimiento _open source_.
    - IBM ofrece modelos _open source_ (Granite) de distintos tipos (lenguaje, visión, seguridad, series de tiempo, geoespaciales), diseñados para correr localmente.

6. **Aceleración del Desarrollo y el Impacto en la Productividad y el Empleo:**
    - El desarrollo de la IA se ha acelerado drásticamente en los últimos 10 años, impulsado por la disponibilidad de datos y la computación en la nube.
    - Esto generará una **explosión de la productividad**. Tareas que antes requerían mucho tiempo ahora se pueden hacer en una fracción del mismo (ejemplo: preparar una presentación).
    - Aunque esto beneficia a las empresas al aumentar la eficiencia del trabajo, para los empleados significa que se esperará que hagan más cosas en el mismo tiempo.
    - La IA está impactando a profesiones de nivel universitario que antes se consideraban menos vulnerables, como el **desarrollo de software** (programadores usan IA para aumentar su productividad en 25-50%, siendo los mejores programadores los que más ganan), la **abogacía** (revisión de documentos, análisis de contratos, investigación de precedentes, aunque es crucial verificar la información), los **recursos humanos** (análisis de currículums, respuesta a preguntas frecuentes vía chatbots, liberando al personal para tareas interpersonales), y la **medicina** (apoyo en diagnóstico, análisis de imágenes, monitoreo de datos vitales de pacientes).
    - El ponente concluye con un mensaje clave: **"la inteligencia artificial no va a reemplazar a las personas pero esas personas sí van a ser reemplazadas por aquellas personas que usen la inteligencia artificial"**. Es vital aprender a utilizar las herramientas de IA disponibles para ser más productivos y competitivos.