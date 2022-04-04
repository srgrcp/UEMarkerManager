# MarkerManager

Gestor de marcador de objetivos para Unreal Engine 4.

# Cómo funciona

## Marker (Componente)

### Agregar un marcador (desde el editor)

Seleccionar cualquier Actor y agregar el componente `Marker`.

![Agregar marcador desde editor](https://github.com/srgrcp/UEMarkerManager/raw/master/Doc/add-marker-from-editor.png)

### Valores por defecto

Al seleccionar el `Marker` del Actor, se podrán configurar 2 parametros: `Marker Text` y `Is Completed`.

`Marker Text` es el texto que se mostrará en el marcador.
`Is Completed` es un booleano que indica si el marcador ya fue completado, en este caso, el marcador se hará invisible, el contador de markadores completos aumentará y el de incompletos disminuirá.

## Marker Manager (Componente)

Componente implementado en el Game Mode, para gestionar los marcadores.

### Interfaz

`Marker Manager` muestra en pantalla de forma dinámica, cuantos marcadores hay en total, cuantos han sido completados y cuantos faltan.

### Agregar y eliminar un marcador (desde blueprints)

El primer paso es obtener la instancia del `Marker Manager` del Game Mode.

![Obtener instancia Marker Manager](https://github.com/srgrcp/UEMarkerManager/raw/master/Doc/get-marker-manager-instance.png)

Seguido de llamar al método `AddMarker` del `Marker Manager` para agregar un marcador (el parámetro `Marker Text es opcional`) o `RemoveMarker` para eliminarlo.

![Llamar métodos](https://github.com/srgrcp/UEMarkerManager/raw/master/Doc/call-add-remove-methods.png)
