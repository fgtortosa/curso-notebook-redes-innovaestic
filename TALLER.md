## Uso de modelos de valoración automatizada (AVM) en el sector inmobiliario con NotebookML


### Objetivos de la Práctica

En esta sesión práctica, exploraremos el funcionamiento y las implicaciones de los Modelos de Valoración Automatizada (AVM) en el sector inmobiliario. Nos centraremos en el conocido caso de *Zestimate* de Zillow para comprender:
*   Cómo funcionan conceptualmente los AVM.
*   Los desafíos y limitaciones de estos modelos.
*   El impacto de las decisiones empresariales en la aplicación de la IA/ML.
*   Cómo utilizar `notebookml` para investigar, analizar y sintetizar información sobre un tema complejo.

## Contexto: El Caso de Zillow y Zestimate

Fundada en 2006, Zillow se consolidó como la plataforma inmobiliaria online líder. Su algoritmo de valoración, *Zestimate*, se convirtió en una referencia. En 2018, Zillow lanzó **Zillow Offers**, una empresa dedicada a la compraventa de viviendas ("iBuying"), confiando en que *Zestimate* le daría una ventaja competitiva.

Sin embargo, tras perder 421 millones de dólares en su negocio de iBuying durante el tercer trimestre de 2021, Zillow cerró esta unidad. El director ejecutivo, Rich Barton, atribuyó parte del fracaso a la incapacidad de la IA para predecir con precisión los precios de las viviendas en un mercado volátil.

Este caso práctico examina la trayectoria de Zillow Offers, analizando factores que contribuyeron a su desaparición, incluyendo las limitaciones de su sistema de IA/ML y cómo el enfoque en el hipercrecimiento por encima de la rentabilidad llevó a desajustes entre las predicciones de precios y las decisiones operativas. Este análisis nos permitirá plantear preguntas importantes sobre el uso adecuado y eficaz de los modelos de IA/ML basados en datos para la toma de decisiones.


## Fase 1: Recopilación y Exploración Inicial de Fuentes

### 1.1. Configuración Inicial: Documentos y Fuentes Web

Comenzaremos cargando un conjunto de documentos y enlaces web que nos servirán como base para nuestra investigación.

**Documentos Fundamentales:**

*   **Explicación del funcionamiento del modelo (Fuentes de Zillow):**
    *   Imputación de datos: `https://www.zillow.com/tech/imputing-data-for-the-zestimate/`
    *   Construcción del Zestimate neuronal: `https://www.zillow.com/tech/building-the-neural-zestimate/`
*   **Investigación académica sobre AVMs:**
    *   University of Oxford Research. The future of automated real estate valuations (AVMs): `https://www.sbs.ox.ac.uk/sites/default/files/2022-03/FoRE%20AVM%202022.pdf`
*   **Opinión pública y análisis del caso Zillow Offers:**
    *   Debate en Reddit sobre la precisión de Zestimate: `https://www.reddit.com/r/FirstTimeHomeBuyer/comments/1e34ygc/how_accurate_are_zillow_zestimates/`
    *   Análisis del cierre de Zillow Offers (JISE): `https://jise.org/Volume35/n1/JISE2024v35n1pp67-72.pdf`
    *   Artículo de CNN sobre la debacle de Zillow: `https://edition.cnn.com/2021/11/09/tech/zillow-ibuying-home-zestimate`

**Acción:**
1.  Descarga los ficheros PDF de los enlaces proporcionados.
2.  En un nuevo notebook de `notebookml`, añade estos PDFs como fuentes.
3.  Añade también las URLs restantes como fuentes web.

### 1.2. Primera Consulta al Notebook

Ahora, realizaremos una primera consulta utilizando *solo una* de las fuentes para entender su contenido específico.

**Acción:**
1.  Selecciona como única fuente el documento "University of Oxford Research. The future of automated real estate valuations (AVMs).pdf".
2.  Realiza la siguiente pregunta al notebook:
    ```
    Háblame sobre el uso de modelos de valoración automatizada (AVM) en el sector inmobiliario. Explica como ejemplo de uso el Zestimate y si el modelo ha funcionado.
    ```
3.  Guarda la respuesta generada por `notebookml` como una nueva **Nota** titulada "Introducción AVMs y Zestimate (Oxford)".

## Fase 2: Ampliación y Profundización con `notebookml`

### 2.1. Uso de la Herramienta "Descubrir"

La herramienta "Descubrir" nos permite ampliar nuestra base de conocimiento sugiriendo fuentes adicionales relevantes. No evaluaremos la calidad intrínseca de cada sugerencia en este paso, sino que exploraremos su potencial.

**Acción:**
1.  Utiliza la función "Descubrir" de `notebookml` con los siguientes prompts (uno a la vez):
    *   `Uso de los Modelos de Valoración Automatizada (AVM) en el sector inmobiliario`
    *   `Quiero conocer más sobre el índice de renta observada de Zillow (Zestimate), si existen algoritmos similares y si hay tecnologías que permitan conocer los precios de la vivienda de manera automática y confiable`
2.  Revisa las fuentes sugeridas por "Descubrir". Añade aquellas que consideres pertinentes a tu notebook.
3.  **(Importante)** Vuelve a activar *todas* tus fuentes (las iniciales y las añadidas mediante "Descubrir").
4.  Realiza nuevamente la pregunta del punto 1.2:
    ```
    Háblame sobre el uso de modelos de valoración automatizada (AVM) en el sector inmobiliario. Explica como ejemplo de uso el Zestimate y si el modelo ha funcionado.
    ```
5.  Compara esta respuesta con la obtenida en el punto 1.2. ¿Cómo ha cambiado la respuesta al tener más fuentes? Guarda esta nueva respuesta en una **Nota** titulada "Visión Ampliada AVMs y Zestimate".

### 2.2. Análisis Detallado y Creación de Notas a partir de Fuentes Específicas
`Notebookml` permite interactuar con cada fuente, mostrando resúmenes y temas clave. Ahora, generaremos notas consolidadas a partir de documentos específicos para facilitar su uso posterior.

**Acción (Resumen del Paper de Oxford):**
1.  Selecciona como única fuente el PDF: "University of Oxford Research. The future of automated real estate valuations (AVMs).pdf".
2.  Pide a `notebookml` un resumen con el siguiente prompt:
    ```
    Crea un resumen del documento. El resumen debe ser extenso, evaluar los temas clave y las relaciones, ya que posteriormente se utilizará como fuente.
    ```
3.  Guarda el resumen generado como una **Nota** titulada "Resumen Extenso - Oxford AVM Future".
4.  **Opcional, pero recomendado para fases posteriores:** Desactiva o elimina el PDF original de las fuentes y añade la **Nota** "Resumen Extenso - Oxford AVM Future" como nueva fuente. Esto agiliza consultas futuras al trabajar con información ya procesada.

**Acción (Resumen del Paper sobre Zillow Offers - JISE):**
1.  Selecciona como única fuente el PDF: "Teaching Case: When Strength Turns Into Weakness... Zillow Offers.pdf".
2.  Pide a `notebookml` un resumen con el siguiente prompt:
    ```
    Resume el texto, explicando las características del Zestimate y sus fallas, así como las circunstancias que rodearon al fracaso del producto iBuying, indicando las causas imputables al algoritmo y las que fueron imputables a la empresa.
    ```
3.  Guarda el resumen como una **Nota** titulada "Análisis Fallo Zillow Offers (JISE)".
4.  Considera reemplazar el PDF original por esta nota como fuente.

**Acción (Análisis de Opinión Pública - Reddit):**
1.  Selecciona como única fuente el enlace de Reddit.
2.  Realiza la siguiente pregunta:
    ```
    ¿Cómo perciben los potenciales clientes al algoritmo Zestimate? ¿Qué problemas detectaron? ¿Cuál fue su funcionamiento real según los usuarios?
    ```
3.  Guarda la respuesta como una **Nota** titulada "Percepción Pública Zestimate (Reddit)".

**Acción (Resumen Técnico de AVMs):**
1.  Activa las fuentes que consideres más técnicas (ej: los artículos de Zillow Tech, la nota del paper de Oxford).
2.  Pide a `notebookml` un resumen técnico con el siguiente prompt:
    ```
    Necesito un resumen TÉCNICO de los algoritmos usados para AVM, separando técnicas en función de su calidad y novedad. El resumen solo debe detallar las características técnicas sin entradillas, resumen final ni citas. Si hay que referenciar algún texto, debe de aparecer al final del resumen en una lista de fuentes usadas en un formato tabla.
    ```
3.  Guarda la respuesta como una **Nota** titulada "Resumen Técnico Algoritmos AVM".

**Acción (Resumen de Problemas y Consecuencias Sociales/Uso):**
1.  Activa las fuentes que traten estos aspectos (ej: CNN, JISE, Reddit, Oxford).
2.  Pide a `notebookml` un resumen con el siguiente prompt:
    ```
    Siguiendo un planteamiento similar al resumen técnico, crea un resumen indicando los problemas detectados con los modelos de valoración automática, especificando los problemas que han causado. Cita las fuentes en el apartado final, en formato tabla, pero sin indicar número de líneas.
    ```
3.  Guarda la respuesta como una **Nota** titulada "Problemas y Consecuencias AVMs".

## Fase 3: Refinamiento y Creación de Contenido Final con `notebookml`

### 3.1. Refinamiento de Notas

Las notas generadas pueden ser aún más pulidas para convertirlas en textos autónomos y bien redactados.

**Acción:**
1.  Selecciona una de las notas creadas (por ejemplo, la "Nota: Problemas y Consecuencias AVMs").
2.  Utiliza el siguiente prompt para refinarla:
    ```
    Transforma este resumen. No utilices bullets ni listados con puntos o apartados. Redacta el texto de manera más legible y literaria, manteniendo una estructura lógica (por ejemplo, hecho -> consecuencia). Elimina las citas del cuerpo del texto para que se pueda guardar como una nota independiente y autocontenida.
    ```
3.  Guarda la versión refinada, quizás sobrescribiendo la anterior o con un nuevo nombre (ej: "Problemas y Consecuencias AVMs - Refinado"). Repite este proceso con otras notas si lo deseas.

**### 3.2. Uso de "Studio" para Síntesis y Materiales de Estudio**

La funcionalidad "Studio" de `notebookml` nos permite crear diversos materiales a partir de las fuentes y notas que hemos curado.

**Acción:**
1.  **Preparación de Fuentes para Studio:** Desactiva todas las fuentes originales (PDFs, URLs) y asegúrate de que *únicamente tus notas curadas y refinadas* estén activas como fuentes. Esto enfocará a "Studio" en el conocimiento que ya has procesado.
2.  **Generación de Materiales:** Utiliza las herramientas de "Studio" para generar:
    *   Una **Guía de Estudio** sobre AVMs y el caso Zestimate.
    *   Una lista de **Preguntas Frecuentes (FAQ)**.
    *   Un **Mapa Conceptual** que relacione los conceptos clave.
3.  **Creación de un Audio Resumen (Podcast):**
    Pide a `notebookml` que genere un guion para un audio resumen con el siguiente prompt:
    ```
    Crea un guion para un audio podcast breve. El tema es sobre los algoritmos de valoración automática de viviendas (AVM). El guion debe incluir: un resumen de la historia de los AVMs (mencionando Zestimate como caso de estudio), sus fortalezas y debilidades. El tono debe ser introductorio, para alumnos que no conocen el tema. Debe fomentar la discusión sobre los aspectos sociales y económicos de estos algoritmos y sus consecuencias a largo plazo. Prepara a los oyentes para una clase práctica donde se debatirá el tema desde un punto de vista de utilidad social y consecuencias. El guion debe estar en español de España, con dos locutores: un hombre (presentador, formula preguntas) y una mujer (experta, responde y da contexto). La mujer también puede hacer una breve introducción inicial.
    ```

## Conclusión de la Práctica y Discusión

Al finalizar esta práctica, deberíamos tener una comprensión más profunda de:
*   La complejidad detrás de los AVMs y los factores que influyen en su éxito o fracaso.
*   Las capacidades de `notebookml` como herramienta de investigación y síntesis.
*   La importancia de la curación de fuentes y la formulación precisa de preguntas (prompts).

**Para la discusión en clase:**
*   ¿Qué otros factores, además de los técnicos, creéis que influyeron en el caso Zillow Offers?
*   ¿Cómo podrían mejorarse los AVMs para ser más fiables y justos?
*   ¿Qué responsabilidades éticas tienen las empresas que desarrollan e implementan estos algoritmos?
*   ¿Cómo imagináis el futuro de la valoración inmobiliaria con la IA?

