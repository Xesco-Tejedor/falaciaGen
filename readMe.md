# 🎭 FalaciaGen: El Generador de Falacias Inteligente

¡Desafía tu pensamiento crítico y explora el arte de la persuasión (y la manipulación)! FalaciaGen utiliza IA para crear falacias personalizadas basadas en tus ideas, completas con su nombre (¡incluso en latín!) y una explicación detallada.

---

## 🤔 ¿Qué es FalaciaGen?

FalaciaGen es una aplicación web interactiva que te permite:

1.  Introducir una **palabra, concepto o frase corta**.
2.  Ajustar un **nivel de "rebuscamiento"** para determinar cuán sutil o compleja será la falacia.
3.  Pulsar un botón y dejar que la **Inteligencia Artificial (a través de OpenRouter.ai)** genere:
    *   Un **texto falaz** convincente relacionado con tu entrada.
    *   El **nombre común** de la falacia empleada.
    *   Su **nombre clásico en latín** (si aplica).
    *   Una **explicación clara** de por qué el argumento es una falacia.

Es una herramienta perfecta para estudiantes de lógica, debate, filosofía, escritores buscando inspiración, o cualquiera interesado en entender mejor los errores de razonamiento y cómo se construyen argumentos engañosos.

---

## ✨ Características Principales

### 🧠 Generación de Falacias por IA
Utiliza modelos de lenguaje avanzados (accesibles vía OpenRouter) para crear contenido original y contextualmente relevante.

### 🎚️ Nivel de Sutileza Ajustable
Controla qué tan obvia o intrincada quieres que sea la falacia generada con un simple deslizador.

### 🔑 Gestión Segura de API Key
Introduce tu API Key de OpenRouter, que se guarda de forma segura en el almacenamiento local de tu navegador (¡nunca se envía a nuestros servidores!).

### 📜 Historial por Término
Cada vez que generas una falacia para un concepto, se guarda en un historial específico para ese término, permitiéndote revisar creaciones anteriores.

### 💾 Exportación a Markdown
Exporta fácilmente el historial de falacias de un término específico a un archivo `.md` bien formateado, ideal para notas o compartir.

### 🎨 Interfaz Limpia y Moderna
Diseño intuitivo y agradable, con indicadores de carga y mensajes de estado claros.

### 📱 Diseño Responsivo
Funciona bien en diferentes tamaños de pantalla (aunque optimizado para escritorio).

### 🚫 Manejo de Errores
Proporciona feedback útil si algo sale mal durante la generación o con la API Key.

### 🌐 Todo en el Navegador
Aplicación 100% frontend. Solo necesitas un navegador web moderno.

---

## 🚀 ¿Por Qué FalaciaGen?

*   **Educativo:** Aprende sobre diferentes tipos de falacias de una manera práctica y entretenida.
*   **Creativo:** Inspírate para escribir, crear personajes argumentativos o simplemente jugar con la lógica.
*   **Concienciación:** Desarrolla un ojo crítico para identificar argumentos falaces en la vida real.
*   **Exploratorio:** Experimenta con las capacidades de la IA en la generación de texto persuasivo y engañoso.

---

## 🛠️ Tecnologías Utilizadas

*   **HTML5:** Para la estructura semántica de la página.
*   **CSS3:** Para el diseño y la apariencia visual (incluyendo variables CSS para fácil tematización).
*   **JavaScript (ES6+):** Para toda la lógica de la aplicación, interacción con el DOM, manejo de API y almacenamiento local.
*   **OpenRouter.ai API:** Como backend para la generación de texto por IA (específicamente usando modelos como `openai/gpt-3.5-turbo` a través de su plataforma).

---

## 🏁 Primeros Pasos y Uso

### 1. Obtén una API Key de OpenRouter
*   Visita [OpenRouter.ai](https://openrouter.ai/keys) y regístrate para obtener una API key. Es necesaria para que la aplicación pueda comunicarse con los modelos de IA.
*   OpenRouter ofrece acceso a diversos modelos, algunos con capas gratuitas o créditos iniciales.

### 2. Configura tu API Key en FalaciaGen
*   Abre el archivo `index.html` en tu navegador web.
*   Ve a la sección "Configuración de API Key".
*   Pega tu clave API en el campo correspondiente y haz clic en "Guardar Clave".
*   La clave se almacenará localmente en tu navegador para futuras sesiones. El botón "Borrar Clave" la eliminará.

### 3. ¡Genera Falacias!
*   **Define tu Base:** Introduce una palabra, concepto o frase corta en el campo de texto (ej: "Redes Sociales", "El éxito", "La tecnología es neutral").
*   **Ajusta el Nivel de Rebuscamiento:** Utiliza el deslizador para indicar cuán sutil o compleja deseas que sea la falacia (0 = muy obvia, 100 = muy rebuscada y difícil de detectar).
*   **Haz clic en "Generar Falacia con IA"**: ¡Y espera la magia!

### 4. Revisa el Resultado
*   El texto de la falacia aparecerá, seguido de su nombre, nombre en latín (si existe) y una explicación.

### 5. Explora el Historial
*   Si has generado falacias para el mismo término anteriormente, aparecerán en la sección "Historial".
*   Puedes exportar el historial del término actual a un archivo Markdown usando el botón "Exportar (MD)".

---

## 💡 ¿Cómo Funciona (Básicamente)?

1.  El usuario introduce un concepto, ajusta el nivel de "rebuscamiento" y proporciona una API Key válida de OpenRouter.
2.  Al hacer clic en "Generar", JavaScript construye un *prompt* detallado. Este prompt instruye a la IA para que actúe como un experto en falacias y genere una basada en el input del usuario, el nivel de complejidad deseado, y que devuelva la respuesta en un formato JSON específico.
3.  Se realiza una petición `fetch` a la API de OpenRouter, enviando el prompt y la API Key.
4.  OpenRouter procesa la petición usando el modelo de IA especificado (ej. GPT-3.5 Turbo).
5.  La IA devuelve una respuesta en formato JSON que contiene el texto de la falacia, su nombre, nombre en latín y explicación.
6.  JavaScript parsea este JSON y muestra la información de forma estructurada en la página.
7.  La generación se guarda en el `localStorage` del navegador, asociada al término de entrada, para la función de historial.

---

## 🚧 Posibles Mejoras Futuras

*   Selección de diferentes modelos de IA disponibles en OpenRouter.
*   Opción para elegir tipos específicos de falacias a generar.
*   Modo "Quiz" para identificar falacias.
*   Mejoras en la interfaz y más opciones de personalización visual.
*   Internacionalización (i18n) para soportar más idiomas.
*   Convertirlo en una Progressive Web App (PWA) para instalación local.

---

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Si tienes ideas para mejorar FalaciaGen, no dudes en:

1.  Hacer un Fork del repositorio.
2.  Crear una nueva rama (`git checkout -b feature/AmazingFeature`).
3.  Hacer tus cambios y hacer commit (`git commit -m 'Add some AmazingFeature'`).
4.  Hacer Push a la rama (`git push origin feature/AmazingFeature`).
5.  Abrir un Pull Request.

Por favor, asegúrate de que tu código sigue las convenciones existentes y está bien comentado.

---

## 📄 Licencia

Distribuido bajo la Licencia MIT. (Se recomienda añadir un archivo `LICENSE` con el texto completo de la licencia MIT a tu repositorio).

---

## 🙏 Agradecimientos

*   A la comunidad de **OpenRouter.ai** por facilitar el acceso a diversos modelos de IA.
*   A los desarrolladores de los **modelos de lenguaje grande** que hacen posible esta magia.
*   A todos los **filósofos y lógicos** a lo largo de la historia que han estudiado y catalogado las falacias.

---

Creado con fines educativos y de exploración. ¡Disfruta generando y aprendiendo!