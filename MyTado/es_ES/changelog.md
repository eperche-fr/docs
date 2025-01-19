# Changelog plugin MyTado

# 01/2025 - Versión 3.1

- Los valores posibles de los diferentes parámetros de los módulos de aire acondicionado ahora se recuperan dinámicamente.  
- Solucionado un problema al recuperar el estado de un dispositivo TadoX cuando está en modo manual durante un período definido.  
- Actualización de la documentación para describir cómo gestionar escenarios con MyTado.

# 12/2024 - Versión 3.0

- Ahora se admiten dispositivos TadoX
- El clima se convierte en un hogar, y la configuración de la conexión se ha trasladado a este dispositivo "hogar"
- Es posible configurar múltiples hogares en caso de poseer tanto dispositivos Tado como TadoX (lo que requiere 2 hogares separados)
- 4 nuevos comandos agregados a los dispositivos Tado(X): activar, desactivar, fecha de la última actualización de datos y nivel de batería
- La gestión de la conexión a Tado ahora utiliza un demonio para evitar tiempos de latencia en PHP

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