# Manual práctico de Linux



[TOC]



## Ejercicios del Capítulo 1

1. Un sistema operativo es:

   a) un programa que permite al usuario realizar tareas específicas

   b) un procesador de textos

   **c) un programa que permite al usuario interactuar con el ordenador y sus componentes** 

   d) ninguna de las respuestas anteriores es correcta.

   

2. Una distribución de Linux es:

   a) el núcleo del SO, junto con un programa de instalación y una selección de aplicaciones

   b) el núcleo del SO, junto con un entorno gráfico y una selección de aplicaciones 

   **c) las dos respuestas anteriores son correctas**

   

3. Cita:

   a) Alguna distribución de Linux buena en el apartado gráfico y en juegos 3D 

   b) Alguna distribución de Linux con servidores preinstalados

   

   **a) Una distribución de Linux con buen apartado gráfico y juegos 3D sería Sabayon**

   **b) Una distribución de Linux con servidores preinstalados sería Slackware**





## Ejercicios del Capítulo 2

1. ¿En qué directorio se encuentran los ficheros de configuración del sistema? 

   **Se encuentran en el directorio /etc.**

   

2. Para entrar en un sistema Linux hace falta:

   a) nombre de usuario, contraseña y dirección IP 

   **b) nombre de usuario y contraseña**  

   c) únicamente una contraseña

   

3. Muestra el contenido del directorio actual. 

   ![image-20251105102753216](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105102753216.png)

   ```bash
   ls
   ```

   

4. Muestra el contenido del directorio que está justo a un nivel superior. 

   ![image-20251105102830364](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105102830364.png)

   ```bash
   ls ..
   ```

   

5. ¿En qué día de la semana naciste?, utiliza la instrucción *cal* para averiguarlo	

      Primero instalamos la apt:		

      ![image-20251105103110311](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105103110311.png)

      ```bash
      sudo apt install ncal
      ```

      Después ejecutamos ncal para ver la fecha de nacimiento:

      ![image-20251105103142693](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105103142693.png)

      ```bash
      ncal
      ```

      

6. Muestra los archivos del directorio /bin

     ![image-20251105103248091](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105103248091.png)

     ```bash
     ls bin
     ```

     

7. Suponiendo que te encuentras en tu directorio personal (/home/nombre), muestra un listado del contenido de /usr/bin:

     a) con una sola línea de comando

     ![image-20251105103421081](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105103421081.png)

     ```bash
     ls /usr/bin --> para listar bin escribiendo la ruta
     ```

     

     b) moviéndote paso a paso por los directorios:  

     ![image-20251105103529735](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105103529735.png)

     ```bash
     cd .. -> para dirigirme al directorio anterior
     ls -> para listar el directorio en el que estoy
     ls bin -> para listar al directorio que escriba
     ```

     

     c) con dos líneas de comandos.

     ![image-20251105103611871](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105103611871.png)

     ```bash
     cd /usr/bin -> como ya estoy en mi usuario y /usr/bin es anterior a este						   vamos ahí
     
     ls -> listarlo
     ```

     

8. Muestra todos los archivos que hay en /etc y todos los que hay dentro de cada subdirectorio, de forma recursiva (con un solo comando).			

      ![image-20251105103701917](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105103701917.png)

      ```bash
      ls -l /etc -> listar con -l 
      ```

      

9. Muestra todos los archivos del directorio /usr/X11R6/bin ordenados por tamaño (de mayor a menor). Sólo debe aparecer el nombre de cada fichero, sin ninguna otra información adicional.

       ![image-20251105104200164](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105104200164.png)

       ```bash
        ls -lS /usr/bin-> listar con -l, ordenar de mayor menor por tamaño con -S
       ```

       

10. Muestra todos los archivos del directorio /etc ordenados por tamaño (de mayor a menor) junto con el resto de características, es decir, permisos, tamaño, fechas de la última modificación, etc. El tamaño de cada fichero debe aparecer en un formato “legible”, o sea, expresado en Kb, Mb, etc.

      ![image-20251105104348424](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105104348424.png)

      ```bash
      ls -lhS /etc -> listar con -l, ordenar de mayor menor por tamaño con -S y vuelve el tamaño a letra con -h
      ```


      ​    

11. Muestra todos los archivos del directorio /bin ordenados por tamaño (de menor a mayor). Sólo debe aparecer el tamaño y el nombre de cada fichero, sin ninguna otra información adicional. El tamaño de cada fichero debe aparecer en un formato “legible”, o sea, expresado en Kb, Mb, etc.

       ![image-20251105104445061](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105104445061.png)

         ```bash
         ls -lhSr /etc -> listar con -l, ordenar de menor a mayor por tamaño con -S y -r de 					 reversed, vuelve el tamaño a letra con -h
         ```

​      

12. Muestra el contenido del directorio raíz utilizando como argumento de ls una ruta absoluta.

    ![image-20251105104704392](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105104704392.png)

      ```bash
      ls / -> listar con / que es el directorio raiz
      ```

      

13. Muestra el contenido del directorio raíz utilizando como argumento de ls una ruta relativa. Suponemos que el directorio actual es /home/elena/documentos.

    Abro escritorio porque los documentos los tenía ahí y la carpeta documentos esta vacia:

      ![image-20251105104852131](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105104852131.png)

      ```bash
      ls /home/scar/Escritorio
      ```

      

14. Crea el directorio gastos dentro del directorio personal.

      ![image-20251105104937633](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105104937633.png)

      ```bash
      mkdir gastos -> con mkdir creamos carpetas
      ```

      

15. ¿Qué sucede si se intenta crear un directorio dentro de /etc?

      ![image-20251105105005041](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105105005041.png)

      ```bash
      mkdir carpeta -> no se puede crear permiso denegado
      ```

      

16. Muestra el contenido del fichero /etc/fstab.

    ![image-20251105105047920](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105105047920.png)

     ```bash
     cat /etc/fstab ->se utiliza para ver el contenido de una archivo de texto
     ```

     

17. Muestra las 10 primeras líneas del fichero /etc/bash.bashrc.	

    ![image-20251105105141902](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105105141902.png)

      ```bash
      head /etc/bash.bashrc -> muestra las 10 primeras líneas de un txt
      ```

      

18. Crea la siguiente estructura de directorios dentro del directorio de trabajo personal:

    Creamos las carpetas:

    ![image-20251105105413041](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105105413041.png)

    Para mostrar en jerarquía de árbol instalamos tree:

    ![image-20251105105452249](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105105452249.png)

    Ejecutamos tree:

    ![image-20251105105341411](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105105341411.png)

      ```bash
      mkdir carpeta -> crear carpeta
      
      cd carpeta -> meterse a carpeta y crear otras dentro de esta con mkdir
      
      sudo apt install tree -> instalar tree
      
      tree -> jerarquía árbol
      ```

      

19. Crea un fichero vacío dentro del directorio musica, con nombre estilos_favoritos.txt

    ![image-20251105105647061](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105105647061.png)

      ```bash
      cd Música 
      
      touch estilos_favoritos.txt -> crear archivo texto vacio
      ```

      

20. Utiliza tu editor preferido para abrir el fichero estilos_favoritos.txt e introduce los estilos de música que más te gusten. Guarda los cambios y sal.

      ![image-20251105105745514](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105105745514.png)

      ```bash
      nano estilos_favoritos.txt -> editar archivo texto, dentro del archivo escribimos y guardamos con Ctrl+S y salimos con Ctrl+X
      ```

      

21. Muestra todo el contenido de estilos_favoritos.txt

     ![image-20251105105913455](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105105913455.png)

     ```bash
     cat estilos_favroritos.txt -> mostrar contenido archivo texto
     ```

     

22. Muestra las 3 primeras líneas de estilos_favoritos.txt

     ![image-20251105105945710](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105105945710.png)

      ```bash
      head -n3 estilos_favoritos.txt -> muestra las 3 primeras líneas del archivo de texto gracias a n3 empezando por el principio (head) 
      ```

      

23. Muestra la última línea de estilos_favoritos.txt

    ![image-20251105110044492](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105110044492.png)

      ```bash
      tail -n1 estilos_favoritos.txt -> muestra la primera línea con n1 empezando por el final (tail)
      ```

      

24. Muestra todo el contenido del fichero estilos_favoritos.txt excepto la primera línea. Se supone que no sabemos de antemano el número de líneas del fichero.

    ![image-20251105110131035](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105110131035.png)

      ```bash
      tail -n+2 estilos_favoritos.txt ->con tail -n+numero muestras desde el número de línea que indiques hasta el final
      ```

      

