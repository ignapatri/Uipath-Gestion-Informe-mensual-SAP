### Proceso informe mensual SAP C13

Generación de un informe de SAP C13, aAñadiendo  los datos a un archivo que se guarda en un directorio de red.

Se realiza el día 1 de cada mes.

#### Proceso

Inicio del bot

Se ejecuta el bot de forma desatendida o atendida, como se prefiera desde el main.xaml 

![Main](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/main.png)

Leemos los settings

Leemos todos los settings del archivo Data y los introducimos en un diccionario para poder usarlos en el proceso

![Settings](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/settings.png)

Iniciamos las aplicaciones

![Settings](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/iniciar.png)

Login process

Para logarnos usamos windows credential, convertimos el password secure string a string para logarnos en sap. 

secure string a string es una actividad creada por mi

![Login](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/login.png)

Gestión de la aplicación

Si el elemento existe, el login es correcto y continúa el proceso del programa, si no es correcto enviamos un email al departamento de sap y paramos el bot

 ![Gestion](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/gestion.png) 

Añadimos la transacción

 ![Transacción](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/transaccion.png) 
 
Gestionamos la fecha

![fecha](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/fecha.png)

Leemos los registros, al ser un proceso que no sabemos cuando concluye, usamos un do while hasta que un elemento aparezca

![log](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/registros.png)

![grabacion](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/grabacion.png)

Exportamos el archivo

![exportar](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/exportar.png)

![exportar](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/select_file.png)

Generamos el archivo

![element exits](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/element_exits.png)

![type into](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/type_into.png)

![generar](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/generar.png)

![wait element](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/wait_element.png)

Mandamos correo al departamento de sap y cerramos sap

![correo](https://github.com/ignapatri/Uipath-Gestion-Informe-mensual-SAP/blob/master/imagenes/correo.png)



















