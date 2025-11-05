# Ejercicios de Forty



[TOC]



## 1 - Trabajo en local

1. Inicializa un nuevo repositorio Git en una carpeta llamada "forty" y agrega los archivos proporcionados en el aula virtual.

   Creamos el repositorio e inicializamos:
   
   ![image-20251104183133429](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104183133429.png)

```bash
 mkdir forty
 cd forty
 git init
```
​	Hacemos un ls para ver los archivos que hemos agregado a la carpeta:

![image-20251104183605018](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104183605018.png)

```bash
ls
```



2. Renombra la rama master a main.

![image-20251104184012445](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104184012445.png)

```bash
git branch -m master main
```



3. Haz que los ficheros README.txt , LICENSE.txt y passwords.txt sean ignorados por el control de versiones.

   Creamos el archivo .gitignore:

   ![image-20251104184716801](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104184716801.png)

   ```bash
   touch .gitignore
   ```

   Añadimos los archivos README.txt, LICENSE.txt y password.txt al archivo .gitignore escribiendo en cada archivo .gitignore:

   ![image-20251104190312563](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104190312563.png)

   ```bash
   echo "README.txt" >> .gitignore
   echo "LICENSE.txt" >> .gitignore
   echo "passwords.txt" >> .gitignore
   ```

   Comprobamos el contenido del archivo .gitignore:

   ![image-20251104190400809](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104190400809.png)

   ```bash
   cat .gitignore
   ```

   Añadimos el cambio:

   ![image-20251104190537413](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104190537413.png)

   ```bash
   git add .gitignore
   ```

   Guardamos el cambio:

   ![image-20251104190506638](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104190506638.png)

   ```bash
   git commit -m "AÑADIDOS README, LICENSE Y password A .gitignore"
   ```

   

4. Crea el archivo passwords.txt . Comprueba que el control de versiones lo ignora.

   El archivo fue creado en el ejercicio anterior.

   Añadimos texto al archivo:

   ![image-20251104190801963](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104190801963.png)

   ```bash
   echo "HOLA" > passwords.txt
   ```

   Comprobamos estado y vemos que es ignorado:

   ![image-20251104190904923](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104190904923.png)

   ```bash
   git status
   ```

   

5. Crea una rama llamada "feature-content" . Muévete a esa rama. Cambia, en la línea 3477, el font-size por 1.5em en el archivo main.css . Confirma cambios y haz commit. Muestra los logs de la forma más gráfica posible.
   Creamos la rama featur-content:

   ![image-20251104191558584](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104191558584.png)

   ```bash
   git branch feature-content
   ```

   Cambiamos a la rama feature-content:

   ![image-20251104191710050](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104191710050.png)

   ```bash
   git checkout feature-content
   ```

   Cambiamos desde VSCode font-size en el archivo main.css:

   ![image-20251104192311583](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104192311583.png)

   Miramos el estado:

   ![image-20251104192349556](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104192349556.png)

   ```bash
   git status
   ```

   Añadimos el cambio:

   ![image-20251104192615866](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104192615866.png)

   ```bash
   git add .
   ```

   Guardamos el cambio:

   ![image-20251104192715446](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104192715446.png)

   ```bash
   git commit -m "LINEA 3477 DEL ARCHIVO MAIN.CSS CAMBIADA"
   ```

   Vemos el historial con un log:

   ![image-20251104193817799](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104193817799.png)

   ```bash
   git log
   ```



6. Elimina el archivo "passwords.txt" en la carpeta forty . Verifica el estado del repositorio. ¿Hay cambios pendientes?

   Borramos el archivo:

   ![image-20251104193114820](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104193114820.png)

   ```bash
   rm passwords.txt
   ```

   Comprobamos estado y vemos que no hay ningún cambio pendiente:

   ![image-20251104193155360](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104193155360.png)

   ```bash
   git status
   ```



7. Crea un nuevo archivo llamado " about.html ", partiendo del archivo generic.html y agrégalo al repositorio, haz un nuevo commit.

   Copiamos el archivo generic.html al archivo about.html:

   ![image-20251104193522482](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104193522482.png)

   ```bash
   cp generic.html about.html
   ```

   Añadimos los cambios:

   ![image-20251104193855800](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104193855800.png)

   ```bash
   git add .
   ```

   Guardamos los cambios:

   ![image-20251104193930226](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104193930226.png)

   ```bash
   git commit -m "REPOSITORIO ABOUT.HTML AGREGADO"
   ```

   Vemos el historial con el log:

   ![image-20251104194027824](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104194027824.png)

   ```bash
   git log
   ```



8. Cambia a la rama main . Examina los logs del repositorio de forma gráfica.

   Cambiamos a la rama main:

   ![image-20251104194451224](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104194451224.png)

   ```bash
   git checkout main
   ```

   Examinamos los logs de forma gráfica:

   ![image-20251104194722372](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104194722372.png)

   ```bash
   git log --graph --oneline --decorate --all
   ```



9. Modifica algo en el archivo generic.html , comprueba que hay cambios, y realiza otro commit . Examina los logs del repositorio de forma gráfica.

   Modificamos el archivo generic.html:

   ![image-20251104195331913](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104195331913.png)

   ```bash
   echo añadir>>generic.html
   ```

   Añadimos los cambios:

   ![image-20251104195627957](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104195627957.png)

   ```bash
   git add generic.html
   ```

   Guardamos los cambios:

   ![image-20251104195742955](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104195742955.png)

   ```bash
   git commit -m "ARCHIVO GENERIC.HTML MODIFICADO"
   ```

   Examinamos los logs de forma gráfica:

   ![image-20251104200024325](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104200024325.png)

   ```bash
   git log --graph --oneline --decorate --all
   ```



10. Modifica algo en el fichero elements.html . Confirma los cambios, pero no hagas commit.

    Modificamos fichero:

    ![image-20251104200213771](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104200213771.png)

    ```bash
    echo añadir>>elements.html
    ```

    Añadimos los cambios, pero no guardamos definitivamente:

    ![image-20251104200709226](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104200709226.png)

    ```bash
    git add .
    ```



11. Mira las diferencias de elements.html . Los cambios no nos gustan, deshaz los cambios de elements.html . Comprueba que no hay cambios pendientes.

    Miramos las diferencias de cambios.html:

    ![image-20251104200952135](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104200952135.png)

    ```bash
    cat elements.html
    ```

    Restauramos el elemento elements.html de la zona staged, es decir el add:

    ![image-20251104201246614](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104201246614.png)

    ```bash
    git restore --staged elements.html
    ```

    Restauramos el contenido como tal del archivo:

    ![image-20251104201332845](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104201332845.png)

    ```bash
    git restore elements.html
    ```



12. Muestra las diferencias entre las dos ramas:

    ![image-20251104202535994](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104202535994.png)

    ```bash
    git diff main..feature-content
    ```



13. Fusiona la rama "feature-content" con la rama principal (main). Muestra los logs del repositorio de una forma gráfica y completa.

    Fusionamos las 2 ramas:

    ![image-20251104205315102](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104205315102.png)

    ```bash
    git merge feature-content
    ```

    Log de forma gráfica y completa:

    ![image-20251104205508847](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104205508847.png)



14. Crea una nueva rama llamada " hotfix " y en ella, corrige un error crítico en el archivo " index.html ". (Por ejemplo, añade el enlace a la nueva página about.html)

    Creamos la nueva rama hotfix:

    ![image-20251104205816443](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104205816443.png)

    ```bash
    git branch hotfix
    ```

    Añadimos enlace a página about.html:

    ![image-20251104210445637](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104210445637.png)

​	Añadimos y guardamos:

![image-20251104210557370](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104210557370.png)

```bash
git add .

git commit -m "ERROR CRÍTICO ARREGLADO EN INDEX.HTML"
```



15. Fusiona la rama "hotfix" con la rama principal y verifica el historial de commits de forma que se vean todas las ramas gráficamente. ¿Borrarías la rama hotfix ? ¿En qué caso? ¿Cómo?

    Fusionamos estas dos ramas:

    ![image-20251104210915295](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104210915295.png)

    ```bash
    git merge hotfix
    ```

    Log de forma gráfica y completa:

    ![image-20251104211048693](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104211048693.png)

    ```bash
    git log --oneline --graph --decorate --all
    ```

​	

​	La borraría porque si ya se fusionó con la principal para que voy a mantenerla.

​	Si esta rama solo se creó para resolver ese error y ya fue resuelto y ahora está en la 	main ya no es necesario.

​	La borraría con el siguiente comando:

```bash
git branch -d hotfix
```



16. Muestra el historial de cambios limitado a los últimos 3 commits.

    ![image-20251104211542669](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104211542669.png)

    ```bash
    git log -3
    ```



17. Etiqueta el commit actual como "v1.0" y muestra las etiquetas existentes.

​	Etiquetamos el commit actual:

​	![image-20251104214256942](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104214256942.png)

​	

```bash
git tag v1.0
```

​	Vemos todos los guit existentes:

​	![image-20251104214322494](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104214322494.png)

​	

```bash
git tag
```

​	













## 2 - Trabajo en remoto

1. Sube al remoto los ficheros de tu repositorio local.

   ![image-20251104215029110](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104215029110.png)

   ```bash
   git remote add origin https://github.com/oscarfd81/forty.git
   
   git push -u origin main
   ```



2. En local, crea una rama 'feature-head'. Cambia el título en la sección head de index.html , borra los comentarios del head , o previos, también. Confirma y sube los cambios al remoto.

   Creamos y nos movemos al mismo tiempo a feature-head:

   ![image-20251104215419349](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104215419349.png)

   ```bash
   git checkout -b feature-head
   ```

   Editamos el archivo index.html con nano index.html:

   ![image-20251104215340877](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104215340877.png)

​	Añadimos y guardamos los cambios del index.html:![image-20251104215633362](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104215633362.png)

```bash
 git add .

git commit "ARCHIVO INDEX ENCABEZADO Y COMENTARIOS MODIFICADO"
```

​	Por último hacemos un push para subir los cambios al repositorio remoto:![image-20251104215754752](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104215754752.png)

```bash
git push -u origin feature-head
```



3. En remoto, crea una rama 'feature-articulo'. Duplica la página generic , nómbrala como articulo.html , y añade como contenido un artículo sobre Git. Confirma los cambios y realiza un commit. Muestra los commits del repositorio tal como se ven en GitHub.

   Rama creada:

   ![image-20251104221223310](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104221223310.png)

   Commits:

   ![image-20251104221129973](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104221129973.png)



4. En el repositorio local examina los cambios. Actualiza el repositorio con el remoto. Fusiona en 'main' las dos ramas 'feature'. Crea la etiqueta 'v2.0'. Muestra los logs, commits, etiquetas y ramas actuales, en local y en remoto.

   Primero descargue las ramas remotas del Git:

   ![image-20251104222215884](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104222215884.png)

   ```bash
   git fetch origin
   ```

   Después me fui a la clase main:

   ![image-20251104222644583](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104222644583.png)

```bash
git checkout main
```

​	Fusionamos clase main con feature:

![image-20251104222758778](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104222758778.png)

```bash
git merge origin/feature-head
git merge origin/feature-articulo
```

​	Creamos etiqueta:

![image-20251104222928092](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104222928092.png)

```bash
git tag v2.0
```

​	Logs commits en local y remoto:

![image-20251104223028768](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104223028768.png)

```bash
git log --oneline --graph --decorate --all
```

​	Ramas en local y remoto:

​	![image-20251104223142704](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104223142704.png)

```bash
git branch -a
```

​	Tags local y remoto:

![image-20251104223230441](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104223230441.png)

```bash
git tag
```



5. En tu copia local, crea una rama nueva . En la rama nueva, cambia los enlaces de la página index.html para que apunten correctamente a la nueva página articulo.html . Confirma los cambios.

   Creamos y nos dirigimos a la nueva rama a la que llame feature-links debido a que los demás se llama feature seguido de lo que sirve cada uno:

   ![image-20251104223419322](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104223419322.png)

   ```bash
   git checkout -b feature-links
   ```

   Actualizamos links index.html:

   ![image-20251104223607784](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104223607784.png)

   ```bash
   nano index.html
   ```

   Añadimos cambios:

   ![image-20251104223704300](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104223704300.png)

   ```bash
   git add .
   ```

   Guardamos cambios:

   ![image-20251104223719028](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104223719028.png)

```bash
git commit -m "ENLACES ACTUALIZADOS EN INDEX.HTML"
```



6. Muestra los logs de forma que se vean las ramas en tu copia local.

![image-20251104223925230](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104223925230.png)

```bash
git log --graph --oneline --decorate --all
```



7. Te gusta el resultado de los cambios. Incorpora los cambios de la rama nueva a la principal.

   Cambio de rama a main:

   ![image-20251104224542459](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104224542459.png)

   ```bash
   git checkout main
   ```

   Fusiono las ramas:

   ![image-20251104224612701](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104224612701.png)

   ```bash
   git merge feature-links
   ```



8. Sube los cambios al remoto borrando la rama nueva , si es necesario. Comprueba primero con un comando en local, las ramas que hay en el repositorio remoto.

   Comprobamos las ramas:

   ![image-20251104224838504](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104224838504.png)

   Lanzamos el main a remoto:![image-20251104224912812](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104224912812.png)

```bash
git push origin main
```



9. Muestra en local los cambios en el archivo index.html entre la versión actual y la anterior.

   El HEAD apunta al commit actual, mientras que el HEAD~1 apunta al commit anterior:

   ![image-20251104225046147](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104225046147.png)

```bash
git diff HEAD~1 HEAD -- index.html
```



10. En el repositorio en GitHub, navega hasta el archivo index.html y selecciona la opción "History".

    ![image-20251104225408764](C:\Users\ferna\AppData\Roaming\Typora\typora-user-images\image-20251104225408764.png)
