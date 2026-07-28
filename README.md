# El costo de una idea — Sorteo (RSJ 2026, Día 2)

Demo interactiva de sorteo de misiones para la actividad del club **AIROS - ESPOL** en el evento
*Ready. Set. Join! 2026*. Es una sola página (`index.html`), sin dependencias externas: usa
tipografía de sistema (nada embebido), así que **funciona sin conexión a internet** una vez
cargada.

## Link público

https://airos-espol.github.io/el-costo-de-una-idea/

Ese link es **permanente**: no cambia aunque se actualice el contenido. Es al que debe apuntar
el código QR impreso en la mesa.

## Cómo actualizar el contenido (sin que cambie el link)

Todo lo editable está al inicio del bloque `<script>` en `index.html`, bien comentado:

- **Banco de misiones inicial** → arreglo `MISIONES_INICIALES`.
- **Cantidad de cartas en modo mazo** → constante `CANTIDAD_CARTAS_MAZO`.

Para que un cambio lo vean **todos** los que escaneen el QR hay que editar el archivo y volver
a publicar:

```bash
git add index.html
git commit -m "Actualizo banco de misiones"
git push
```

GitHub Pages republica solo en 1–2 minutos. El link no cambia.

> El panel de administración (ícono discreto en la esquina superior derecha) sirve para ajustes
> durante la jornada: activar/desactivar misiones, agregar, editar, eliminar, restaurar el banco
> original y activar el modo mazo. Esos cambios se guardan en `localStorage` de **ese
> dispositivo** — sobreviven a recargar la página, pero no se comparten con los celulares que
> escanean el QR. Lo permanente se hace editando el código.
