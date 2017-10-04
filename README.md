# Servicio Monitoreo Colas V1.0
El servicio se encarga de notificar mediante correo electronico el encolamento de mensajes en una determinada cola AMQ.

## Prerequisitos
El servicio necesita de las siguientes features instaladas en el contenedor
- camel-http4
- camel-quartz2
- camel-dozer
- camel-jackson

El profile debe tener el archivo de propiedades llamado "monitoreoCola"

### Contenido archivo monitoreoCola

```
# Informacion cola para monitoreo
datos.cola.ip= <dirección ip de la cola que se desea monitorear>
datos.cola.puerto=<puerto de la cola que se desea monitorear>
datos.cola.brokerName=<Nombre del broker de la cola que se desea monitorear>
datos.cola.destinationName=<nombre de la cola que se desea monitorear>
datos.cola.username=<Username para el acceso amq a traves de jolokia>
datos.cola.password=<Contraseña para el acceso amq a traves de jolokia>
datos.cron.monitoreo=<Cron que indica cada cuando se ejecutara la ruta camel>
datos.cola.limite.mensajes=<Limite de mensajes desde el cual se empezara a notificar por e-mail>

# Informacion cola error
datos.cola.error.brokerURL=<Direccion URL TCP del broker asociado a la cola de errores>
datos.cola.error.username=<Usuario para enviar el mensaje a la cola de errores>
datos.cola.error.password=<Password del usuario>
datos.cola.error.amq.fault=<Nombre cola de errores>

# Informacion para envio de email
datos.mail.direccion.servicio.mail=<Direccion URL del servicio de email>
datos.mail.destinatario=<Correo electronico del usuario el cual sera notificado>
datos.mail.remitente=<Correo electronico del remitente>
datos.mail.subject=<Asunto del e-mail>
datos.mail.canal=<Canal solicitado por el servicio>
datos.mail.plantilla=<Plantilla del e-mail>
```

### EndPoint de la ruta camel

- Cola AMQ: AMQ.FAULT
- Servicio de envio de correo electronico: http://10.20.74.63:7801/ServicioEnvioEmail

## Versionamiento
El codigo fuente se encuentra en el siguiente repositorio git

```
Repogit
```


