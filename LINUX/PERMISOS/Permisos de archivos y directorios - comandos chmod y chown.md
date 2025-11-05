# Permisos de archivos y directorios - comandos chmod y chown

[TOC]

## Cuestiones resueltas

1. ¿Qué permisos otorga chmod 640 informe.txt ?

   ![image-20251105101226690](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105101226690.png)

   ```bash
   chmod 640 -> el primer grupo se refiere a usuario y le da privilegio de -rw (lectura=4 y escritura=2), el segundo grupo se refiere al grupo en el que se encuentra el usuario y le da el privilegio de -r (lectura=4) y el último 	grupo se refiere al resto de usuarios y no da ningún privilegio
   ```

   

2. ¿Qué hace el comando *chmod u=rw, g=rw, o= archivo.txt*?

   Este comando atribuye al usuario privilegios de lectura y escritura, al grupo lo mismo y a los demás usuarios nada.

   

3. Cambia script.sh para que: El propietario pueda leer, escribir y ejecutar, El grupo solo leer, Los demás nada.

   ![image-20251105101818361](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105101818361.png)

   ```bash
   chmod u=rw,g=x,o= script.sh
   ```

   

4. Cambia el propietario de /var/www a usuario apache y grupo www-data

   ![image-20251105102027870](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105102027870.png)

   ```bash
   sudo chown apache:www-data /var/www
   ```

   

5. ¿Qué permisos deja el comando chmod a+x *.sh?

   A todos los usuarios (a=all), se les da permiso de ejecucion(x) sobre todos los archivos .sh.

   

6. Un directorio debe permitir: al propietario todo, al grupo entrar y listar y a otros nada

   ![image-20251105102221242](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105102221242.png)

   ```bash
   chmod u=rwx,g=rx,o= carpeta1
   ```

   

   ![image-20251105102307896](C:\Users\2dawd08\AppData\Roaming\Typora\typora-user-images\image-20251105102307896.png)

```bash
ls-l -> con este comando vemos todos los permisos atribuidos
```







