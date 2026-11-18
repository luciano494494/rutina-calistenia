# Rutina de Calistenia

Una app para seguir tu rutina de entrenamiento desde el celular. Lee tu planilla de Google Sheets (pegando el link o subiendo el Excel) y te muestra **solo el día y la semana que te tocan**, con los videos, el RPE, las repes que hiciste y tus comentarios.

Funciona dentro de **Claude** (claude.ai): cada persona publica su propia copia y sus datos quedan guardados en su cuenta.

## Qué hace

- Cargás la rutina **pegando el link de tu planilla** o subiendo el Excel. Si vino del link, con **Actualizar desde la planilla** traés los cambios del entrenador.
- Abre directo en la sesión que te toca (Día y Semana).
- Muestra la rutina por bloques (Super Serie A, B, C…), con Reps, Series, Carga, Tempo y Aclaraciones.
- Cargás el **RPE** de cada ejercicio (6 a 10, o "No llegué") y las **repes que hiciste**.
- **Marcar día completo**: lo que quedó sin RPE pasa a "No llegué con el tiempo".
- Te avisa qué RPE te quedaron sin cargar en días anteriores.
- Podés **editar la rutina** tocando cualquier dato de la tabla, agregar o quitar ejercicios.
- Comentario por día.

## Cómo instalarla en tu Claude

### 1. Descargá el archivo

Descargá [`rutina.html`](rutina.html): abrilo y tocá el botón de descarga (**Download raw file**, la flecha hacia abajo arriba a la derecha).

### 2. Pedile a Claude que la publique

1. Entrá a [claude.ai](https://claude.ai) (en la web o en la app).
2. Abrí un chat nuevo y **adjuntá el archivo `rutina.html`**.
3. Pegá este mensaje:

> Publicá este archivo como artifact, sin cambiar el código, declarando las capacidades `db`, `user` y `mcp` con el servidor "Google Sheets" y la herramienta `get_spreadsheet`. Después pasame el link.

4. Claude te va a dar un link. Esa es tu app.

### 3. Cargá tu rutina

**Opción A: con el link (recomendada)**

1. Conectá **Google Sheets** en Claude, una sola vez: en claude.ai → Configuración → Conectores → Google Sheets → Conectar. Usá la cuenta de Google que puede ver tu planilla.
2. En Google Sheets, copiá el link de tu planilla (**Compartir → Copiar vínculo**, o la dirección de la barra del navegador).
3. En tu app, pegalo en el recuadro y tocá **Cargar desde el link**. La primera vez, Claude te pide permiso para que la app use Google Sheets: aceptalo.
4. Elegí el mes y tocá **Usar esta rutina**.

**Opción B: con el Excel**

1. Descargá tu planilla como Excel:
   - **En la compu:** Archivo → Descargar → Microsoft Excel (.xlsx).
   - **En el celular:** los tres puntos ⋮ → Compartir y exportar → Guardar como Excel.
2. En tu app, tocá **Elegir archivo .xlsx**, subí el Excel y elegí el mes.

Para cargar otro mes u otra planilla, tocá **Cambiar rutina** (arriba, debajo del cartel del día).

### 4. Tenerla a un toque en el celular

En Safari (iPhone) o Chrome (Android), abrí el link de tu app → **Compartir** → **Agregar a pantalla de inicio**.

## Cómo actualizarla cuando salga una versión nueva

1. Descargá el `rutina.html` nuevo de este repositorio.
2. En claude.ai, adjuntalo y pegá:

> Publicá este archivo en mi artifact existente [pegá acá el link de tu app], sin cambiar el código, declarando las capacidades `db`, `user` y `mcp` con el servidor "Google Sheets" y la herramienta `get_spreadsheet`.

**Importante:** publicala **en el mismo link**. Si Claude crea una app nueva, no vas a ver lo que ya tenías cargado.

## Qué tiene que tener tu planilla

La app está hecha para planillas con este formato:

- Una celda que dice **EJERCICIOS** por cada día, con **DIA 1**, **DIA 2**… arriba.
- A la derecha, por cada semana, las columnas **Reps, Series, Carga, tempo, RPE, Aclaraciones**.
- Filas **SUPER SERIE A / B / C** que agrupan los ejercicios.

Si tu planilla tiene otro formato, la app te va a avisar que no encontró ninguna rutina.

## Preguntas frecuentes

**¿Dónde se guardan mis datos?**
En tu cuenta de Claude, dentro de tu propia copia de la app. Nadie más los ve. Si tu cuenta no permite guardar datos en las páginas publicadas, la app los guarda en el navegador de tu teléfono: siguen funcionando, pero no se sincronizan entre dispositivos y se pierden si borrás los datos del navegador.

**¿Funciona con una cuenta gratis de Claude?**
No está probado. Si te funciona (o no), contalo en [Sugerencias](https://github.com/luciano494494/rutina-calistenia/issues/new).

**¿La app cambia mi planilla de Google Sheets?**
No. Solo la lee (con el link o con el Excel). Lo que cargás o editás queda en la app.

**Si vuelvo a cargar la rutina o toco "Actualizar desde la planilla", ¿pierdo algo?**
Se reemplaza la rutina por la de la planilla, así que se pierden las ediciones que hiciste en la tabla. Los RPE, repes y comentarios se mantienen mientras el mes tenga el mismo nombre.

**El link no me funciona.**
Revisá que Google Sheets esté conectado en tu Claude, con una cuenta que pueda ver la planilla. Si no, usá la opción del Excel.

## Sugerencias y problemas

Abrí un issue en [github.com/luciano494494/rutina-calistenia/issues](https://github.com/luciano494494/rutina-calistenia/issues/new) (necesitás una cuenta de GitHub, es gratis).
