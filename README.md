# Descripción

Generador de sala de control online y enlaces para concursantes online.

# Características

- No requiere programas adicionales ni conocimientos técnicos
- Crea un espacio aislado para cada concursante y un único espacio de monitorización para los vigilantes
- Autoconfigura el espacio de concursante
- Autoconfigura la sala de control
- Autoconfigura la seguridad del sistema
- Permite a los vigilantes una sencilla e intuitiva identificación y seguimiento de las pantallas y webcams de los concursantes
- Organización automática de las cámaras
- Servicio de chat para comunicación entre los vigilantes y los concursantes, y viceversa
- Servicio de conversación por voz y vídeo para comunicación entre los vigilantes y los concursantes, y viceversa
- Avisos de notificaciones para los vigilantes y para los concursantes
- Permite múltiples vigilantes
- Respetuoso con la privacidad
- No guarda ningún dato ni grabación

# Instalación

- Acceder con el navegador a http://raw.githack.com/olimpiada-informatica/online-proctor-wizard/master/ o bien copiar el archivo `index.html` a la ruta donde se instalará y acceder a ella con el navegador.
- En el archivo `index.html` se pueden modificar las variables globales `settings` y `labels` para adaptar el asistente a las necesidades concretas. La utilidad de las propiedades de `settings` son las siguientes:
  - `vdo_ninja_url`: URL donde se alojan los servicios de VDO.ninja. Solo cambiar si se utiliza un servidor VDO.ninja autohospedado
  - `vdo_ninja_url_encryption`: URL donde se alojan los servicios de cifrado de URL para los servicios de VDO.ninja. Solo cambiar si se utiliza un servidor VDO.ninja autohospedado
  - `vdo_ninja_url_encryption_key`: Clave para usar en el cifrado de la URL. Solo cambiar si se utiliza un servidor VDO.ninja autohospedado
  - `room_title_prefix`: Título de la página de la sala de control, también usado para la página del asistente. Cualquier cadena Unicode es válida
  - `room_favicon`: Imagen para mostrar como ícono de la página y logotipo en la sala de espera. Debe ser una URL válida
  - `room_name_prefix`: Prefijo para usar en las salas de concursante, debe ser único para cada uso. Solo se permiten letras y números, sin espacios
  - `pwd_min_length`: Longitud mínima permitida para la contraseña de la sala. Mín: 0
  - `pwd_generate_length`: Longitud de las contraseñas de sala generadas con el generador de contraseñas
  - `num_contestants`: Número de concursantes. Mín: 1
  - `teams`: Nombres de los equipos. Para cada uno, cualquier cadena Unicode es válida
  - `langs`: Códigos de idioma ISO 639 Set-1 (2 letras) y el nombre del idioma
- Las propiedades de las variables `settings` y `labels` se pueden sobreescribir pasándo su valor en formato JSON como parámetros URL.

# Aclaración sobre la seguridad
 - El punto más débil de la seguridad del sistema es la encriptación de la URL. Este encriptación es reversible, aunque hacerlo no es trivial. Un concursante podría llegar a acceder a esta sala y en tal caso observar a los concursantes rivales. Para detectar esta situación (que debería ser fácilmente detectable observando los monitores de los concursantes) en la sala de control se muestra cuántos vigilantes hay contectados en todo momento.
 - Para evitar perder la contraseña maestra, el generador de contraseñas se deshabilita si el campo contraseña tiene valor o se ha generado ya una


-----


# Description

Generator of online control room and online contestants links.

# Features

- No additional software or technical skills required
- Creates an isolated space for each contestant but a single monitoring room for proctors
- Auto-configures the contestant's space
- Auto-configures the control room
- Auto-configures system security
- Provides proctors with a simple and intuitive identification and tracking of contestants' screens and webcams
- Automatic organization of cameras
- Chat service for communication between proctors and contestants, and vice versa
- Voice and video conversation service for communication between proctors and contestants, and vice versa
- Notification alerts for proctors and contestants
- Allows multiple proctors
- Privacy-respectful
- Does not store any data or recordings

# Installation

- Access via the browser at http://raw.githack.com/olimpiada-informatica/online-proctor-wizard/master/ or copy the `index.html` file to the path where it will be installed and access it with the browser.
- In the `index.html` file, you can modify the global variables `settings` and `labels` to adapt the wizard to specific needs. The description of each `settings` property:
  - `vdo_ninja_url`: URL where the VDO.ninja services is hosted. Only change if using a self-hosted VDO.ninja server
  - `vdo_ninja_url_encryption`: URL where the URL encryption services for VDO.ninja services is hosted. Only change if using a self-hosted VDO.ninja server
  - `vdo_ninja_url_encryption_key`: Key to use to encrypt the URL. Only change if using a self-hosted VDO.ninja server
  - `room_title_prefix`: Title of the proctor page, also used for the wizard page. Any Unicode string is valid
  - `room_favicon`: Image to display as page icon and logo in the waiting room. Must be a valid URL
  - `room_name_prefix`: Prefix to use for rooms, must be unique for each use. Only letters and numbers are allowed, no spaces
  - `pwd_min_length`: Minimum allowed length for the room password. Min: 0
  - `pwd_generate_length`: Length of room passwords generated with the password generator
  - `num_contestants`: Number of contestants. Min: 1
  - `teams`: Names of the teams. For each, any Unicode string is valid
  - `langs`: ISO 639 Set-1 (2-letters) language codes and the name of the language
- The properties of the `settings` and `labels` variables can be overridden by passing their value in JSON format as URL parameters.

# Disclaimer on security

- The weakest point of the system's security is the URL encryption. This encryption is reversible, although doing so is not trivial. A contestant could potentially access the control room and observe rival contestants. To detect this situation (which should be easily spotted by observing the contestants' monitors), the control room displays how many proctors are connected at all times.
- To avoid losing the master password, the password generator is disabled if the password field has a value or if one has already been generated.
