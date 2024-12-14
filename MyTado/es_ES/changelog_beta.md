# Changelog plugin MyTado - beta

# 12/2024 - Versión 3.0

- Ahora se admiten dispositivos TadoX
- El clima se convierte en un hogar, y la configuración de la conexión se ha trasladado a este dispositivo "hogar"
- Es posible configurar múltiples hogares en caso de poseer tanto dispositivos Tado como TadoX (lo que requiere 2 hogares separados)
- 2 nuevos comandos agregados a los dispositivos Tado(X): la fecha de la última actualización de datos y su nivel de batería

# 04/11/2024 - Versión 2.0

- La gestión de la conexión a Tado ahora utiliza un demonio para evitar tiempos de latencia en PHP

# 30/10/2024 - Versión 1.6

- Los errores en la recuperación de las capacidades de un objeto de tipo AC ya no bloquean la recuperación de otros objetos

# 17/10/2024 - Versión 1.5

- La potencia de calefacción ahora se recupera y se muestra
- Ahora es posible cambiar la denominación predeterminada de los dispositivos conectados Tado
- Traducción al español añadida

# 13/10/2024 - Versión 1.4
- Corrección de errores: Se añadió un nombre predeterminado a los comandos meteorológicos
- Las diferentes versiones del mismo tipo de modelo de objeto conocido ahora se configuran de la misma manera

# 25/05/2024 - Versión 1.3
- Añadido el manejo de dispositivos de aire acondicionado y calentadores de agua
- Añadida la traducción al alemán

# 08/05/2024 - Versión 1.2
- Los comandos activar/desactivar se reemplazan por el comando 'modo' de tipo información y por el comando 'set_mode' de tipo acción
- El widget de los dispositivos se actualizó en consecuencia

# 05/05/2024 - Versión 1.1
- Añadidos comandos para activar/desactivar módulos y para definir una temperatura manualmente
- Primera versión de los widgets

# 25/04/2024 - Versión 1.0
- Primera versión estable