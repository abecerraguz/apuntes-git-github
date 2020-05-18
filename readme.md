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



