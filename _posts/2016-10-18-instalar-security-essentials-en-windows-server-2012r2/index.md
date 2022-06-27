---
title: "Instalar Security Essentials en Windows Server 2012R2"
date: "2016-10-18"
categories: 
  - "informatica"
  - "tutoriales"
tags: 
  - "antivirus"
  - "tutorial"
  - "windows-security-essentials"
  - "windows-server-2012"
coverImage: "/assets/posts/mse.png"
thumbnail-img: "/assets/posts/mse.png"
---

Que **Windows 8** trajo consigo un sinfín de **cambios y mejoras** es algo indiscutible, a pesar de que algunas de ellas no tenminaran de convencer a los usuarios (un ejemplo de ello es la intefaz Metro **Modern UI**).

Sin embargo, otra de las novedades es que al fin incluía una solución **antivirus** integrada: **Windows Defender**.

El problema es que dicha suite solo estaba integrada en las versiones para escritorio.

**Windows Server 2012** **no incluyó dicha suite** por no estar destinada a un ámbito de servidores. Eso solo deja la opción de adquirir una solución antivirus de terceros o, en caso de no querer gastar dinero, optar por instalar una solución gratuita con las molestias que conllevan. Además, existen pocos antivirus gratuitos que funcionen en Windows Server.

Por eso vamos a explicar cómo **instalar Windows Security Essentials en Windows Server** 2012 / 2012R2.

Aunque Windows Defender no es descargable por estar integrado con Windows 8, sí que podemos descargar e instalar la versión instalable para Windows 7, Windows Security Essentials, lo que si bien puede no ser la mejor solución por lo menos permite funcionar un motor y unas bases de datos actualizadas de manera gratuita y sin publicidad.

Si intentamos instalarlo directamente nos mostrará el siguiente mensaje de fallo, ya que detecta que nuestro Sistema Operativo no es Windows 7:

![avir001](/assets/posts/images/avir001-e1476639866986.png)

Para solucionarlo, tendremos que activar la ejecución en **modo compatibilidad**. Hacemos clic derecho en el instalador y clicamos en "Propiedades". Después, en la pestaña de compatibilidad, marcamos "Ejecutar este programa en modo de compatibilidad para:" y seleccionamos Windows 7 en el desplegable:

![avir002](/assets/posts/images/avir002-e1476640018141.png)

Pulsamos el botón aceptar y acto seguido abrimos el intérprete de comandos, pulsando en el botón inicio y escribiendo "Símbolo del sistema". Una vez abierto tendremos que ir a la carpeta donde se encuentra el instalador e introducir el siguiente comando:

> `mseinstall /disableoslimit`

![avir003](/assets/posts/images/avir003-1.png)

Ahora sí que se se iniciará el instalador de Windows Security Essentials:

![avir004](/assets/posts/images/avir004-e1476640053250.png)

Una vez finalizada la instalación se descargarán las últimas definiciones de virus y spyware:

![avir005](/assets/posts/images/avir005-e1476640097312.png)

Tras terminar es recomendable realizar un **escaneo completo** de nuestro sistema para asegurarnos de que está libre de amenazas. Al ser un escaneo completo puede tardar un buen rato en completarse, por lo que podemos seguir trabajando mientras tanto. Una vez haya terminado la interfaz de Security Essentials mostrará el siguiente mensaje:

![avir006](/assets/posts/images/avir006-e1476640192100.png)

Lo he probado una infinidad de veces en servidores en producción sin problema alguno excepto a la hora de desinstalarlo (pronto hablaremos de eso).

Este método puede sacarnos de más un apuro. Sin embargo **lo recomendable** para cualquier empresa seria y que valore la integridad de sus datos **es invertir en seguridad informática**. Como mínimo, un paquete integrado de seguridad de alguna empresa reputada.
