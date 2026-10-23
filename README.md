# Test Utópico de Poti · v0.8

Versión del prototipo con un motor de comparación basado en señales conceptuales, contradicciones explícitas y desempates adaptativos. Diseñada para GitHub Pages y uso local en navegador.

## Biblioteca integrada

- 778 pensadores únicos y 864 fichas dimensionales.
- Las fichas están integradas en el HTML autosuficiente; `pensadores_catalogo.json` se entrega como exportación de los datos.
- El motor compara el vector de respuestas con todos los perfiles de la dimensión correspondiente, no solo con una pequeña lista manual.

## Cambios en v0.8

- Nuevo motor de afinidad que combina similitud general, cobertura de señales del perfil, señales explicadas y penalización por contradicciones modeladas.
- Capa de afirmaciones conceptuales: los perfiles con más detalle muestran formulaciones asociadas a conceptos y, en algunos casos, una obra de referencia.
- La evidencia visible distingue coincidencias y posibles tensiones. La ausencia de una tensión detectada no significa que no exista una discrepancia filosófica.
- Fichas exploratorias reciben un límite de puntuación y están etiquetadas como afinidad de tradición, no como comparación individual documentada.
- Preguntas adaptativas cuando los tres resultados principales están cerca y hay etiquetas distintivas suficientes para diferenciar las hipótesis. Se evita inventar una pregunta de desempate si las fichas no contienen diferencias identificables.
- Respuestas de desempate se guardan por separado y se incorporan al ranking. Se mantienen respuestas anteriores si existen en el almacenamiento local; el nuevo formato usa `utopia-poti-v08`.
- Interfaz en catalán, castellano e inglés.

## Límites metodológicos

Los porcentajes son puntuaciones heurísticas, no probabilidades estadísticas ni medidas científicamente validadas. Muchos perfiles del catálogo siguen siendo exploratorios y heredarán señales amplias de una tradición. Las afirmaciones con obra de referencia son orientativas, no una revisión de fuentes académicas ni citas exhaustivas. Para que el test alcance rigor alto, cada perfil exploratorio debe evolucionar hacia tesis individualizadas, referencias verificables y registro explícito de controversias/contraevidencia.

## Archivos incluidos

- `index.html`: aplicación autosuficiente, con motor y catálogo incrustados.
- `pensadores_catalogo.json`: exportación del catálogo dimensional.
- `manifest.webmanifest` e iconos: metadatos e iconos de la aplicación.
- No se utiliza un service worker en esta versión para evitar que una versión antigua quede retenida en caché.

## Publicar

Sustituye el `index.html` en la raíz del repositorio y confirma con **Commit changes**. No es necesario subir el JSON para el funcionamiento del cálculo.
