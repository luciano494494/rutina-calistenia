# Rutina de Calistenia

Una app para seguir tu rutina de entrenamiento desde el celular. Lee el Excel de tu planilla y te muestra **solo el día y la semana que te tocan**, con los videos, el RPE, las repes que hiciste y tus comentarios.

Funciona dentro de **Claude** (claude.ai): cada persona publica su propia copia y sus datos quedan guardados en su cuenta.

## Qué hace

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

> Publicá este archivo como artifact, sin cambiar el código, declarando las capacidades `db` y `user`. Después pasame el link.

4. Claude te va a dar un link. Esa es tu app.

### 3. Cargá tu rutina

1. Abrí tu planilla de entrenamiento en Google Sheets.
2. Descargala como Excel:
   - **En la compu:** Archivo → Descargar → Microsoft Excel (.xlsx).
   - **En el celular:** los tres puntos ⋮ → Compartir y exportar → Guardar como Excel.
3. Abrí tu app, tocá **Elegir archivo .xlsx**, subí el Excel y elegí el mes.

### 4. Tenerla a un toque en el celular

En Safari (iPhone) o Chrome (Android), abrí el link de tu app → **Compartir** → **Agregar a pantalla de inicio**.

## Cómo actualizarla cuando salga una versión nueva

1. Descargá el `rutina.html` nuevo de este repositorio.
2. En claude.ai, adjuntalo y pegá:

> Publicá este archivo en mi artifact existente [pegá acá el link de tu app], sin cambiar el código y manteniendo las capacidades `db` y `user`.

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
No. Lee el Excel que subís y nada más. Lo que cargás o editás queda en la app.

**Si vuelvo a subir el Excel, ¿pierdo algo?**
Se reemplaza la rutina por la del archivo, así que se pierden las ediciones que hiciste en la tabla. Los RPE, repes y comentarios se mantienen mientras el mes tenga el mismo nombre.

## Sugerencias y problemas

Abrí un issue en [github.com/luciano494494/rutina-calistenia/issues](https://github.com/luciano494494/rutina-calistenia/issues/new) (necesitás una cuenta de GitHub, es gratis).
