# <img src="../images/MyHeatzy_icon.png" width="60"/> Plugin MyHeatzy

El plugin **MyHeatzy** permite recuperar datos de tus dispositivos conectados Heatzy.

Los datos se actualizan regularmente según el cron seleccionado (entre 5 y 30 minutos).

---

> **Dispositivos compatibles**
>
> Actualmente solo se admiten completamente los modelos Pilote y Glow (independientemente de su versión).
> Para dispositivos no compatibles o si experimentas problemas, consulta la sección [En caso de problemas](#en-caso-de-problemas).

---

# Configuración

## Configuración del plugin

1. Ve a la configuración del plugin.
2. Instala las dependencias.
3. Inicia el demonio.

Si el demonio no se inicia, puede que el puerto por defecto (59769) ya esté en uso. En ese caso, elige un puerto libre (por ejemplo: 59770), guarda y reinicia el demonio. Si el problema persiste, consulta [En caso de problemas](#en-caso-de-problemas).

También debes completar (y guardar):
- Tu identificador de usuario de Heatzy.
- Tu contraseña de acceso a Heatzy.
- Frecuencia de actualización: cron 5, 10, 15 o 30 minutos (solo uno activo). Mantén también el cron diario.

Una vez introducidos correctamente los datos, los dispositivos se sincronizarán automáticamente. Cierra la configuración. Si no aparecen, actualiza la página o revisa los registros.

## Configuración de dispositivos

> **RECORDATORIO**
>
> Usa el comando **Sincronizar** para recuperar nuevos dispositivos agregados o compatibles tras una actualización del plugin.

### Dispositivos Heatzy conectados
<img src="../images/Pilote.png" width="60"/><img src="../images/Glow.png" width="60"/>

Al hacer clic en un dispositivo Heatzy puedes acceder a:

- **Nombre del equipo**: el nombre que configuraste en la app Heatzy.
- **Objeto padre**: según tu organización.
- **Categoría**: elige la categoría adecuada.

Pestaña **Comandos**:
- Lista de comandos disponibles.
- Posibilidad de guardar los valores numéricos.
- Actualización manual con el comando **Actualizar**.

El widget del dashboard muestra la imagen del equipo, información y su configuración actual.

Modos disponibles:
- **Confort**
- **Eco**
- **Antihielo**
- **Apagado**

Además, según el equipo:
- Activar modo "boost"
- Activar modo "vacaciones"
- Establecer temperatura deseada (primero cambia a modo Eco o Confort)
- Activar/desactivar programación

---

# Gestión de escenarios

¡Cambia al modo Eco o Confort antes de fijar una temperatura en tus escenarios! (solo en ciertos equipos).

---

# En caso de problemas

1. Cambia los registros de **MyHeatzy** a modo **debug**.
2. Reinicia el demonio.
3. Consulta los registros para encontrar el problema.

Si es necesario, revisa [FAQs](#faqs) y [Pedir ayuda](#pedir-ayuda).

## FAQs

### Error Fatal: [Errno 98] address already in use

El puerto por defecto (59769) está en uso. Cámbialo por otro (por ejemplo, 59770) y reinicia el demonio.

## Pedir ayuda

1. Revisa si tu problema ya está en la [comunidad Jeedom](https://community.jeedom.com/tag/plugin-myheatzy)

2. Si no, crea un nuevo tema.

3. Proporciona siempre:
   - Tu configuración Jeedom
   - Los modelos de Heatzy utilizados
   - Registros completos de **MyHeatzy** y **MyHeatzy_daemon** (adjuntos, con modo debug)

> **Oculta cualquier dato personal en los registros antes de publicarlos**

# Otras recomendaciones

1. Deja una opinión en el market si te gusta el plugin.
2. ¡Propón mejoras al desarrollador!

---

**¡Gracias por usar el plugin MyHeatzy!**

Tu opinión es valiosa para seguir mejorándolo 😊
