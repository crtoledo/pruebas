# Servicio Monitoreo Colas
El servicio se encarga de notificar mediante correo electronico el encolamento de mensajes en una determinada cola AMQ.

## Prerequisitos
El servicio necesita de las siguientes features instaladas en el contenedor
camel-http4
camel-quartz2
camel-dozer
camel-jackson

El profile debe tener el archivo de propiedades llamado "monitoreoCola"

### Contenido archivo monitoreoCola
