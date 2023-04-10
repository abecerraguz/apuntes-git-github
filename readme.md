# Comandos para movernos dentro del terminal (Comandos o acciones) son los siguientes:

   - La utilizaremos para controlar las versiones de nuestro proyecto 
   - Estructura de directorio
   - La Raiz de los nodos esta definida por el "/".
   - Una de las cosas mas importantes es saber en que directorio estamos trabajando:
   
        - pwd + enter ( Nos muestra en que directorio estamos trabajando ).
        - ls + enter ( Nos muestra la lista del directorio padre ).
        - ls -a + enter ( Nos muestra los archivos ocultos )
        - cd + enter ( Nos permite navegar entre directorios )
        - cd nombreDirectorio/ nos lleva al directorio Raiz
        - cd .. ( Nos vuelve atras o directorio padre ).
        - cd Documents ( Nos lleva a la carpeta Documentos )
        
# Anatomia de un comando

- pwd (Nombre del comando), algunos comando tienen un argumento como por ejemplo:
- cd Desktop ( Desktop es el argumento ).
- ls -a ( Algunos comandos tienen opciones es el caso del - o a veces -- )

# Administración de archivos y carpetas desde el terminal

- mkdir + ( Nombre del directorio ) crea un directorio ejemplo. 
- mkdir proyecto1
- touch + ( Nombre del archivo ) crea un archivo con la extension "html".
- touch index.html     
- cp + ( Nombre del archivo este copia el archivo ) ejemplo:
    - cp index.html proyecto1/index.html
    - cp index.html proyecto1/index2.html ( Crea una copia del archivo original ).
- cp index.html index3.html ( Copia otro archivo dentro del directorio ).     
- Copiar un directorio dentro de otro.
    - mkdir assets
    - cp -r assets proyecto1    
- rm ( Importante borra sin ir a la papelera )
- rm archivo.extension : Borra un archivo.
- rm -r directorio : Borra un directorio de manera recursiva (borra el directorio y sus   archivos y directorios internos).
- rm .* , remueve todos los temporales

# INSTALAR GIT

## Instalando GIT

Abrir el Terminal o GitBash escribir lo siguiente.

~~~

	$ brew install git

~~~

## Version de Git 

Para ver la version de Git instalada

~~~
	
	git --version

~~~

## Configurar Git 

Para configurar git escribir el usuario y la contraseña de GitHub

~~~	
git --global user.name "username" 
git --global user.email "ingresecorreo@gmail.com"
~~~

## Iniciar un proyecto en Git 

Para iniciar un proyecto en Git debo desplazarme al proyecto de la carpeta a traves del Terminal y luego escribir los siguientes comandos:


~~~
	  
	  
	  Paso uno vas a la carpeta que vas iniciar con git ejemplo git cd Desktop/mi_carpeta, luego:

	  git init
	  git add .
      git commit -m "Mi pimer commit"

      Paso dos, Ir al HTML hacer un cambio, luego nuevamente:

      git add .
      git commit -m "Segundo commit"
      
      Paso Tres para ver el estado de los commit puedo escribir lo siguiente:

      git status
      git log


~~~

## Para crear una git pages 

~~~

	git branch gh-pages

~~~

## Eliminar git desde un proyecto

~~~

	rm -rf .git

~~~

# Crear clave SSH para sincronizar GIT y GITHUB

~~~

	Paso 1 ingresar en el terminal correo que ingresaste en github, Enter
	ssh-keygen -t rsa -b 4096 -C "tu_correo@gmail.com"

	Paso 2 Luego te pregunta donde va a quedar alojada tu llave solo dale Enter

	file in which to save the key (/Users/alejandro_becerra/.ssh/id_rsa): 

	Paso 3 Luego Como yo ya tengo una Llave me pregunta si deseo sobre escribir la que tengo, te recomiendo que le digas que si. o sea ingresa "y" y enter.

	Overwrite (y/n)?

    Paso 4 Copia la clave en la memoria cache del computador con este comando en el terminal

    Comando para MAC 
    pbcopy < ~/.ssh/id_rsa.pub

    Comado para WINDOW 
    clip < ~/.ssh/id_rsa.pub

    Paso 6 ir a Github registrarse y luego ir a setting (Esta en el icono de perfil extrema derecha hacer click seleccionar setting). Ir al menu izquierdo y seleccionar la opción "SSH and GPG Keys", luego seleccionar la opción "New SSH Key" y Pegar la clave copiada desde el terminal.

~~~



