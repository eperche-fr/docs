# Changelog plugin MyTado - beta

# 19/03/2025 - Versión 5.1

- Reorganización de la visualización de la página de equipos  
- Se resolvió un problema con la sincronización durante una nueva instalación del complemento  
- Corrección de la visualización de la imagen para los dispositivos del modelo RU02B (RU02 gestiona el termostato y el agua caliente)  


# 09/03/2025 - Versión 5.0

- Reestructuración de la gestión de configuración de equipos para una mayor flexibilidad en el futuro, independientemente de las versiones del plugin.
- Se han añadido equipos de tipo **usuarios** para obtener detalles sobre la ubicación de los usuarios de Tado en sus escenarios.
- Ahora es posible personalizar las imágenes de los usuarios, que se mostrarán en el widget **casa** cuando estén presentes.
- Posibilidad de elegir la frecuencia de actualización de los datos.

# 20/02/2025 - Version 4.1

- Para los dispositivos **TadoX**, la temperatura mostrada ahora es la **medida por el dispositivo** (y no la de la zona).
- El **widget de casa Tado** ahora muestra **el número de personas presentes**.

# 16/02/2025 - Versión 4.0

- El demonio ahora se basa en el módulo JeedomDaemon de Mips, que elimina cualquier fuga de memoria.
- El equipo del hogar tiene una nueva acción que permite saber cuántos usuarios están en casa.
- Los objetos con múltiples roles (por ejemplo: control de caldera y calentador de agua) ahora se representan con un equipo por función.
- Los parámetros de las acciones ahora están disponibles durante las pruebas de comandos y en los escenarios.

# 19/01/2025 - Versión 3.1

- Los valores posibles de los diferentes parámetros de los módulos de aire acondicionado ahora se recuperan dinámicamente.  
- Solucionado un problema al recuperar el estado de un dispositivo TadoX cuando está en modo manual durante un período definido.  
- Actualización de la documentación para describir cómo gestionar escenarios con MyTado.

# 12/2024 - Versión 3.0

- Ahora se admiten dispositivos TadoX
- El clima se convierte en un hogar, y la configuración de la conexión se ha trasladado a este dispositivo "hogar"
- Es posible configurar múltiples hogares en caso de poseer tanto dispositivos Tado como TadoX (lo que requiere 2 hogares separados)
- 4 nuevos comandos agregados a los dispositivos Tado(X): activar, desactivar, fecha de la última actualización de datos y nivel de batería

# 11/2024 - Versión 2.0

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