# 📑 Indice

- [Capítulo 1](#capitulo-1)
  - [Introducción](#introduccion)
  - [¿Qué necesitamos?](#que-necesitamos)
  - [Packet Tracer](#packet-tracer)
  - [¿Qué son las Redes/Network?](#que-son-las-redesnetwork)
    - [Construyendo una Red de computadoras](#construyendo-una-red-de-computadoras)
    - [Clientes y Servidores](#clientes-y-servidores)
    - [Switches](#switches)
    - [Routers](#routers)
    - [Firewalls](#firewalls)
    - [Resumen](#resumen)

# Capítulo 1

## Introducción.

Al ser este el primer capítulo, me gustaría hacer una pequeña introducción al libro: por qué lo estoy escribiendo y a quién va dirigido.

Estoy escribiendo este libro como forma de **repaso antes de rendir el examen de la CCNA** y también como **método de estudio personal**.

Decidí escribirlo y hacerlo público por dos motivos:

1. Porque al explicar los conceptos, aprendo y los fijo mejor
2. Porque a alguien mas le puede llegar a servir.

Por lo tanto, si lo encontrás útil, te pido por favor que lo compartas con alguien que creas que también le pueda servir.

Este libro va dirigido a:

- Personas que quieran rendir la **CCNA.**
- Personas que quieran aprender sobre **Redes / Networks.**

Algo que recomiendo para quienes quieren rendir la CCNA es que

**consuman el material en inglés**, ya que el examen está completamente en ese idioma. Si utilizan cursos en inglés, se van a ir familiarizando con el vocabulario técnico.

Por esta misma razón, yo también voy a incluir el vocabulario en inglés a lo largo del libro.
Mi idea es hacer este libro **lo más práctico posible**, explicando los conceptos mientras realizamos laboratorios.
Al final de cada capítulo vas a encontrar otro laboratorio para reforzar lo aprendido.
En este capítulo vamos a aprender **qué son las redes (networks)** construyendo una red simple, e introduciendo los principales conceptos que se utilizan en redes.

## ¿Qué necesitamos?

Para empezar vamos a necesitar:

1. **Una PC o laptop** para poder hacer los laboratorios. La buena noticia es que no necesitás una computadora potente, ya que vamos a usar **Packet Tracer**, que solo requiere 4 GB de RAM y 1.4 GB de espacio libre en disco.
2. **Descargar Packet Tracer**, un programa de Cisco que simula redes.
    
    Podés encontrarlo en:
    
    [https://www.netacad.com/resources/lab-downloads?courseLang=en-US](https://www.netacad.com/resources/lab-downloads?courseLang=en-US)
    
    Cisco también tiene un curso corto donde enseña a descargarlo, instalarlo y usarlo:
    
    [https://www.netacad.com/courses/getting-started-cisco-packet-tracer?courseLang=en-US](https://www.netacad.com/courses/getting-started-cisco-packet-tracer?courseLang=en-US)
    

Recomiendo hacerlo antes de seguir con este libro, aunque también te voy a explicar cómo usarlo.

## Packet Tracer

![image.png](/resources/cap-1/download-packet.png)

Una vez que entres en la página de descarga, elegí el instalador correspondiente a tu sistema operativo.

En mi caso es **Windows 11**, así que selecciono el último disponible.

El archivo se descargará (normalmente en la carpeta *Downloads*). Vamos al directorio, lo ejecutamos y seguimos los pasos:

1. Aceptamos el acuerdo (*agreement*) y hacemos clic en **Next**.

![image.png](/resources/cap-1/license-agreement.png)

1. Elegimos la carpeta de instalación (yo la dejo por defecto) y clic en **Next**.

![image.png](/resources/cap-1/select-dest.png)

1. Elegimos si queremos accesos directos; también lo dejo por defecto.

![image.png](/resources/cap-1/start-menu.png)

![image.png](/resources/cap-1/addition-tasks.png)

1. Finalmente, clic en **Install**.

![image.png](/resources/cap-1/ready-install.png)

Y el programa va a comenzar a instalarse

![image.png](/resources/cap-1/installing.png)

Una vez instalado, hacemos clic en **Finish** y Packet Tracer se abrirá automáticamente.

![image.png](/resources/cap-1/completed.png)

Antes de usarlo por primera vez, el programa te preguntará si querés autorizar el modo *multi-user*.
Yo elegí **No**.

![image.png](/resources/cap-1/packet-tracer-window.png.png)

Y listo, ya tenemos el programa abierto.

# ¿Qué son las Redes/Network?

Para definir las las redes de computadoras (networks), voy a usar la definición de wikipedia y luego vamos a crear una red paso a paso en Packet Tracer.

Una **red de computadoras**, **red de ordenadores** o **red informática** es un conjunto de [equipos nodos](https://es.wikipedia.org/wiki/Hardware_de_red) y [software](https://es.wikipedia.org/wiki/Software) conectados entre sí por medio de [dispositivos físicos](https://es.wikipedia.org/wiki/Hardware_de_red) que envían y reciben [impulsos eléctricos](https://es.wikipedia.org/wiki/Corriente_el%C3%A9ctrica), [ondas electromagnéticas](https://es.wikipedia.org/wiki/Radiaci%C3%B3n_electromagn%C3%A9tica) o cualquier otro medio para el transporte de [datos](https://es.wikipedia.org/wiki/Dato), con la finalidad de compartir información, recursos y ofrecer [servicios](https://es.wikipedia.org/wiki/Servicio_de_red).

![image.png](/resources/cap-1/nodes-icons.png)

Antes de comenzar a analizar la definicion, quiero que recuerdes estos **nodos** (iconos) con sus nombres ya que los vamos a estar utilizandon en todo el curso.

**Client and Server** también son conocidos como ***end hosts*** 

### Construyendo una Red de computadoras.

Si todavia no abriste Packet Tracer, es momento de hacerlo.

 Una vez abierto dirigite a la parte inferior izquierda donde estan todos los dispositivos. 

![image.png](/resources/cap-1/net-devices.png)

Y elegí **End Devices.**

![image.png](/resources/cap-1/end-hosts.png)

Ahora arrastrá **dos PCs** al área de trabajo.

Las PCs, laptops, teléfonos y tablets son considerados **clientes (clients)**, ya que son los dispositivos desde los cuales accedemos a servicios.

Sin embargo, un cliente también puede actuar como **servidor (server).**

.

![image.png](/resources/cap-1/add-pcs.png)

En la imagen de arriba tenemos dos clientes, pero todavía no tenemos una red. Para crearla, tenemos que **conectarlas con un cable.**

.
Por ahora, usá el ícono del **rayo**, que permite a Packet Tracer elegir automáticamente el tipo de cable correcto (más  delante vamos a ver los distintos tipos de cables).

![image.png](/resources/cap-1/select-cable.png)

eleccioná el rayo, conectá **PC0** con **PC1** y ya vas a tener tu primera **Network**.

![image.png](/resources/cap-1/connect-cable.png)

### Clientes y Servidores

Como mencione antes, una de las PCs puede actuar como  **cliente** y la otra como **server**:

- Un **cliente (client)** es un dispositivo que accede a un servicio dispobible en un servidor, por ejemplo un celular, una computadora, una laptop, ect.
- Un **servidor (server)** es un dispositivo que provee **servicios o funciones**  a los clientes. Por ejemplo, las paginas web se encuentran en un servidor y los cliente acceden a ellas desde sus computadoras o celulares, etc.

Usemos como ejemplo el **Bluetooth**. 

Imaginá que querés pasarle unas fotos de tu celular al celular de tu amigo. 

- Tu celular, que **tiene las fotos y las comparte**, actúa como **servidor**.
- El celular de tu amigo, que **recibe las fotos**, actúa como **cliente.**

Aunque ambos celulares sean “clientes” en general, en ese momento cada uno cumple un rol distinto (uno es servidor y el otro el de cliente)

Ahora imaginemos que querés ver un video en YouTube o leer las noticias en una página web.

En ese caso, tu PC (el cliente) **envía una solicitud a Internet** para llegar al servidor, y luego el servidor **responde con los datos solicitados**.

![Animation.gif](/resources/cap-1/packet-to-server.gif)

Sé paciente, que más adelante vamos a aprender a hacer la animación pero este no es el momento.

Así que vamos a crear este ejemplo. Vamos a elegir una PC, un router (que va a actuar como Internet) y un servidor, y los conectamos con un cable, como aprendiste anteriormente. Recuerda que el router lo vas a encontrar en **“Network Devices”**, y la PC y el servidor en **“End Devices”**.

![image.png](/resources/cap-1/internet-router.png)

Cuando el servidor responde, no envía todos los datos juntos, sino **en partes pequeñas** (paquetes), hasta completar el contenido (por ejemplo, el video).

### Switches

Supongamos ahora que en tu casa u oficina tenés dos computadoras y una impresora. Para conectar todos los dispositivos al mismo tiempo vamos a usar un **Switch**

.

[Cisco Catalyst 2960](/resources/cap-1/switches-catalyst-2960-series-switches-alt2.avif)

Cisco Catalyst 2960

Así que vamos a **Packet Tracer** y elegimos **dos PCs**, **una impresora (Printer)** y **un switch**.

![image.png](/resources/cap-1/select-switch.png)

Una vez que tengas los dispositivos igual que en el diagrama de arriba, los conectamos con un cable y nos tiene que quedar así.

![image.png](/resources/cap-1/connect-2-sw.png)

Los **switches** tienen las siguientes características:

- Tienen varias interfaces/puertos para conectar diferentes dispositivos.
- Reenvían datos entre su propia Red Local / LAN (Local Area Network).
- Todos los dispositivos conectados a un **switch** perteces a la misma LAN.
- No reenvían datos fuera de su LAN, por ejemplo a Internet.

Por eso, si queremos que una PC se comunique con un servidor fuera de su LAN, vamos a necesitar un **router (enrutador).**

### Routers

Ahora imaginemos que tenemos una pequeña empresa con oficinas en Buenos Aires, pero por cuestiones de costos enemos los servidores —donde guardamos toda la información de la empresa— en otra ciudad, por ejemplo, en São Paulo, Brasil.

Y vamos a armar este diagrama en packet tracer.

![image.png](/resources/cap-1/offices.pngcap-1/)

Para ello, elegimos la opción para dibujar rectángulos o cuadrados, y el color que queramos. Seguimos los pasos de la imagen de abajo.

![image.png](/resources/cap-1/image%2018.png)

En mi caso, elegí amarillo y verde. Para poder escribir, elegimos la opción **“Place Notes”** o presionamos la tecla **“n”**, y hacemos clic en la parte donde queramos escribir.

![image.png](/resources/cap-1/image%2019.png)

Para que la oficina de Buenos Aires, Argentina, pueda comunicarse con los servidores de São Paulo, necesitamos utilizar un router (enrutador). Este dispositivo sirve para conectar diferentes redes locales entre sí o para enviar los datos a Internet.

Así que vamos a armarlo, y te quedaría así. Creo que a estas alturas ya podés hacerlo por tu cuenta.

![image.png](/resources/cap-1/image%2020.png)

![Animation.gif](/resources/cap-1/Animation%201.gif)

Por lo tanto, como se ve en la animación de arriba, la PC1 envía el paquete al Router1, el Router1 lo envía al Router2, el Router2 lo envía al Server2, y luego el Server2 responde.

Las principales características de los **routers** son:

- Tienen menos interfaces/puertos que los **switches.**
- Sirven para conectar LANs entre si y envían paquetes hacia otras redes o hacia Internet.

![Router Cisco 8200 series](/resources/cap-1/image%2021.png)

Router Cisco 8200 series

### Firewalls

Ahora bien, ya tenemos las dos oficinas conectadas entre sí, la de Buenos Aires y la de São Paulo, pero para que puedan comunicarse, deben hacerlo a través de Internet, ya que no se va a tender un cable de una oficina a la otra. Al estar en Internet, que es una red pública, pueden existir actores maliciosos (hackers o ciberdelincuentes) que quieran robar nuestros datos.

Entonces, para tratar de evitar que algún intruso ingrese a nuestra red, utilizamos un dispositivo de seguridad llamado **firewall**.

Los firewalls son dispositivos de red que filtran el tráfico según las reglas con las que se configuran. Al principio, los firewalls filtraban el tráfico según el número de IP, y básicamente el tráfico de la red de la empresa hacia afuera estaba permitido, pero el tráfico de fuera hacia la red de la empresa era bloqueado.

También hay softwares que funcionan como firewalls, por ejemplo, el firewall de Windows. Este tipo de firewall se llama **host-based firewall**.

Y los nuevos firewalls tienen características más avanzadas; por ejemplo, también pueden funcionar como **IPS (Intrusion Prevention System)**.

Siguiendo el último diagrama, vamos a conectar los firewalls. Estos pueden estar conectados dentro de la LAN, es decir, antes del router, o fuera de la LAN, después del router.

![image.png](/resources/cap-1/image%2022.png)

Ahí es donde se encuentra el firewall; por lo tanto, vamos a usar dos firewalls: uno para São Paulo y otro para Buenos Aires, colocando uno dentro de la LAN —en mi caso, el de São Paulo estará dentro de la LAN y el de Buenos Aires fuera de la LAN—. Recuerda que, para poder conectarlos, vas a tener que eliminar el cable con la tecla **“Del”** y conectar un cable nuevo.

![image.png](/resources/cap-1/image%2023.png)

Las principales características de los **firewalls** son:

- Monitorean y controlan el **tráfico** de la red según las reglas configuradas.
- Pueden estar dentro de la LAN o fuera de la LAN.
- Los **Next-Generation firewalls** son firewalls que tienen **características** más avanzadas.
- Los **host-based firewalls** son programas (softwares) que filtran el **tráfico** que entra y sale de una PC.

**Modelos de firewall:**

![Cisco ASA](/resources/cap-1/image%2024.png)

Cisco ASA

[Cisco Firepower.](/resources/cap-1/security-firepower-1000-series.avif)

Cisco Firepower.

### Resumen

En este capítulo aprendimos qué son las redes de datos: básicamente, **nodos (dispositivos)** que se comunican entre sí.

También conocimos los principales dispositivos que componen una red:

- **Cliente (Client):** dispositivo que accede a un servicio (por ejemplo, una laptop o un celular).
- **Servidor (Server):** dispositivo que provee servicios o funciones (por ejemplo, un servidor web).
- **Switch:** conecta varios dispositivos dentro de una misma LAN.
- **Router:** conecta distintas redes o LANs entre sí, o con Internet.
- **Firewall:** dispositivo de seguridad que filtra el tráfico de red según reglas configuradas.