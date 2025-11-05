# Configuración de VirtualBox - Instalación de la máquina Cliente Ubuntu



[TOC]



## 1 - Configuración de VirtualBox

Lo primero es poner modo *Expert*

![expert](C:\Users\ALUMNO\Downloads\VirtualBox - Preferences 2025-09-19 10.47.57.png)

Vamos a añadir una red tipo NAT para poder conectar varias máquinas virtuales:

![image-20250919105658781](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250919105658781.png)

Configuramos la red:

![image-20250919105448003](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250919105448003.png)

## 2 - Creación de la máquina cliente en Ubuntu

Establecemos los parámetros de la nueva máquina:

![image-20250919110549693](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250919110549693.png)



![image-20250919110837429](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250919110837429.png)

​		![	](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250919110949674.png)



Podemos ver la nueva máquina:

![image-20250919111236577](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250919111236577.png)

Cambiamos algunos ajustes:

- En la **Descripción** guardamos el usuario y la contraseña de la máquina.				![image-20250919111500999](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250919111500999.png)

- Deshabilitamos el **Audio**:

  ![image-20250919111803985](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250919111803985.png)

- El adaptador de red debe ser **NAT**:

  ![image-20250919121204427](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250919121204427.png)

  

## 3 - INICIAMOS LA MÁQUINA VIRTUAL

  Elegimos el idioma, zona horaria... y creamos nuestra cuenta

  ![image-20250919122450017](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250919122450017.png)

  Una vez elegidas todas las opciones procedemos a la instalación:

  ![image-20250919122533399](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250919122533399.png)

  

## 4 - Instalación de las Carpetas Compartidas

  Ejecutamos este comando una vez hayamos actualizado todo con update y upgrade:

  ![image-20250924094722447](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250924094722447.png)

  Ejecutamos este comando:

  ![image-20250924095142322](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250924095142322.png)

  Ejecutamos este comando para carpetas compartidas:

  ![image-20250924095213245](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250924095213245.png)





## 5 - Instalación de las Guest Additions

​	Ejecutamos este comando una vez hayamos actualizado todo con update y upgrade:

![image-20250924095916308](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250924095916308.png)	

​	Insertar CD y pulsamos en Upgrade Guest Additions:

​	![image-20250924100355834](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250924100355834.png)![image-20250924100739532](C:\Users\ALUMNO\AppData\Roaming\Typora\typora-user-images\image-20250924100739532.png)



​	

​	