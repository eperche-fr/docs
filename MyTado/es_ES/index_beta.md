# <img src="docs/images/MyTado_icon.png" width="60"/> Plugin MyTado

El plugin **MyTado** permite recuperar los datos de tus dispositivos conectados Tado, así como la información meteorológica gestionada por Tado.

La actualización de estos datos se realiza cada 30 minutos.

>**Equipos gestionados**
>
>Los dispositivos de los modelos AC0X, BU0X, RU0X y VA0X son completamente compatibles (en principio, independientemente de su versión). Para los demás modelos, solo tendrás acceso a las funcionalidades básicas (acceso a la temperatura medida, activación/desactivación/modo automático, actualización de datos).
>Para cualquier dispositivo no soportado hasta la fecha, contacta al desarrollador especificando el modelo que tienes y las funcionalidades faltantes, así como cualquier información que consideres útil.

# Configuración

## Configuración del plugin

Debes rellenar absolutamente los siguientes 3 campos:
1) la dirección de correo electrónico utilizada para crear tu cuenta en Tado
2) la contraseña definida
3) el nombre exacto (sensible a mayúsculas y minúsculas) de tu casa en la aplicación Tado

La unidad de medida de temperatura es opcional. **El Celsius es la unidad por defecto**.

Finalmente, después de guardar tu configuración, inicia la sincronización de tu casa con la opción **Sincronización**.

## Configuración de los equipos

>**INFORMACIÓN**
>
>Solo necesitas usar el comando **Sincronización** para obtener todos tus dispositivos conectados y el acceso a la información meteorológica gestionada por Tado.

### Tus dispositivos conectados Tado <img src="docs/images/AC0X.png" width="60"/><img src="docs/images/BU0X.png" width="60"/><img src="docs/images/RU0X.png" width="60"/><img src="docs/images/VA0X.png" width="60"/>

Al hacer clic en un dispositivo conectado Tado, llegarás directamente a su página de configuración:

- **Nombre del equipo**: Nombre del equipo basado en su número de serie.
- **Objeto padre**: Indica el objeto padre al que pertenece el equipo. Depende de ti definirlo.
- **Categoría**: Permite elegir la categoría del equipo.

Al hacer clic en la pestaña **Comandos**, encontrarás la lista de todos los comandos disponibles, así como la posibilidad de historizar los valores numéricos.
Los datos se actualizan cada 30 minutos, pero puedes forzar la actualización bajo demanda con el comando **refresh**.

El widget muestra la imagen correspondiente a tu equipo, así como la información y configuración actual de tus equipos.
También puedes definir el modo de funcionamiento de tu dispositivo:
- 'Automático': Se tiene en cuenta la programación realizada en la aplicación Tado;
- 'Manual': Ofrece la posibilidad de salir del modo automático y definir el(los) parámetro(s) de tu elección;
- 'Apagado': El dispositivo está completamente apagado.

>**Información importante**
>
>En el caso de un cambio manual de la temperatura deseada, esta se aplicará a todos los dispositivos presentes en la misma zona que tu dispositivo (así es como funciona Tado).

### El clima de Tado <img src="docs/images/WeatherEq.svg" width="60"/>

Al hacer clic en el clima de Tado, llegarás directamente a su página de configuración:

- **Nombre del equipo**: Nombre del equipo por defecto.
- **Objeto padre**: Indica el objeto padre al que pertenece el equipo. Depende de ti definirlo.
- **Categoría**: Permite elegir la categoría del equipo.
- **Latitud**: Latitud referenciada en Tado para tu casa y utilizada para recuperar el clima correspondiente.
- **Longitud**: Longitud referenciada en Tado para tu casa y utilizada para recuperar el clima correspondiente.

Al hacer clic en la pestaña **Comandos**, encontrarás la lista de todos los comandos disponibles, así como la posibilidad de historizar los valores numéricos y el estado meteorológico.
Los datos se actualizan cada 30 minutos, pero puedes forzar la actualización bajo demanda con el comando **refresh**.

El widget muestra el tiempo en forma de imagen, así como la temperatura y la luminosidad actual.