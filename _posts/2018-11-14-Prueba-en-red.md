---
layout: post
title: "Proyecto 2: Probando en red"
comments: true
date:   2018-10-23 11:58:00 -0600
category: proyectos
numero: 2
descripcion: >
 Instrucciones para probar utilizando Hamachi.
---

# Hamachi
Hamachi es un programa que nos permite crear VPN (redes virtuales). Estas redes nos permitirán probar el proyecto entre computadoras distintas sin importar las condiciones de la red local (por ejemplo, el wifi galileo no nos permite conectarnos entre máquinas).

**Aviso importante: El siguiente tutorial menciona instalar algunos programas en Windows. Usaremos Windows solo por la interfaz gráfica de Hamachi, porque allí es más fácil leer los datos que nos interesan.**

**NO usaremos Java en Windows, la comunicación en red se complica por el firewall. Ubuntu no da problemas. Si insisten en usar Java en Windows, ustedes son los responsables de resolver sus propios problemas de red.**

# Crear una red

1. Crear una cuenta gratuita en [vpn.net](https://www.vpn.net/), en la esquina superior derecha donde dice Sign In. Las cuentas gratuitas permiten conectar hasta cinco máquinas.
2. Descargar Hamachi para Windows en [vpn.net](https://www.vpn.net/). En Windows tenemos interfaz gráfica, entonces es más fácil configurar.
3. Instalar Hamachi y hacer click en el botón de encendido. Nos pedirá que realicemos log in, y lo hacemos usando los datos que ingresamos al registrarnos.
4. Elegir la opción crear nueva red (solo lo hacemos una vez), colocarle nombre y alguna contrasena sencilla.

![Paso 4](/assets/imgs/hamachi01.png) ![Paso 4](/assets/imgs/hamachi02.png)

# Unirse a una red

Nos uniremos a la red desde nuestras computadoras con Linux.

1. Ingresar a [vpn.net/linux](https://www.vpn.net/linux) desde nuestra computadora con Linux. 
2. Descargar Hamachi, si usan Ubuntu 64-bits deben descargar `logmein-hamachi_2.1.0.VersionMasReciente_amd64.deb`.
3. Buscar el archivo descargado y hacerle doble clic. Se abrirá una ventana de Ubuntu Software, hacer clic en la opción para instalar.
4. Hamachi ya está instalado! Podemos escribir `hamachi --help` en nuestra terminal y se mostrará el menú de ayuda.
5. Ahora configuraremos Hamachi. Usar el comando `sudo hamachi login` en la terminal para autenticarnos, no necesitamos colocar nombre de usuario ya que solo nos uniremos.
6. Luego de hacer log in nos uniremos a la red. Usamos el comando `sudo hamachi join nombreDeMiRed passwordDeMiRed`.
7. En la computadora con Windows, comprobar que alguien se unió a la red.
8. Se recomienda cambiar de nombre usando `sudo hamachi set-nick apodoDeMiComputadora` para reconocer bien cuál es cada máquina.

# Usar la red
![IP](/assets/imgs/hamachi03.png)

En la interfaz gráfica de Windows pueden revisar cuál es la dirección asignada de cada máquina (usen set-nick para que sea más fácil reconocer cada computadora!).
En este caso, `25.52.61.198` es la IP de mi computadora con Windows. `25.53.43.243` es la IP de mi máquina con Ubuntu. Utilicen estas IP en donde corresponda en sus programas de Java.
