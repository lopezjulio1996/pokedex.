
     1. Preparación del Entorno
	Descargar y extraer el repositorio:
Baja el archivo comprimido del repositorio de GitHub.
Extrae el contenido del archivo descargado.
	Explorar la carpeta del proyecto:
Accede a la carpeta pokedex-angular que se encuentra dentro del archivo extraído.

2. Configuración del Proyecto en Visual Studio Code

	Abrir el proyecto en Visual Studio Code:
Inicia Visual Studio Code.
Ve a Archivo -> Abrir Carpeta y navega hasta la carpeta pokedex-angular.
Instalar las dependencias necesarias:
Abre una terminal en Visual Studio Code (Terminal -> Nueva Terminal).
Ejecuta el comando npm install y espera a que todas las dependencias se instalen correctamente.

3. Construcción del Proyecto

	Compilar el proyecto:
En la terminal, ejecuta el comando npm run build.
Este comando generará la carpeta dist que contiene los archivos necesarios para desplegar la aplicación en Azure.

4. Despliegue en Azure

	Comprimir y subir la carpeta dist a Azure:
Comprime la carpeta dist en un archivo .zip.
Crea una aplicación web en Azure con el nombre teheranPokedex.
Accede a la sección de Herramientas de desarrollo en el portal de Azure.
Selecciona Consola de depuración y luego CMD.
Arrastra y suelta el archivo .zip en la consola y descomprímelo.
	Resolver problemas de carga de imágenes:
Si las imágenes no se cargan correctamente, asegúrate de que la carpeta assets esté ubicada correctamente dentro de pokedex-angular y que se haya subido adecuadamente.

5. Agregar Seguridad a la Aplicación

Crear y configurar web.config:
Dentro de la carpeta desplegada, crea un archivo llamado web.config.
Agrega las siguientes directivas de seguridad al archivo
<?xml version="1.0" encoding="UTF-8"?>
<configuration>
    <system.webServer>
        <httpProtocol>
            <customHeaders>
                <add name="X-Frame-Options" value="DENY" />
                <add name="X-XSS-Protection" value="1; mode=block" />
                <add name="X-Content-Type-Options" value="nosniff" />
                <add name="Strict-Transport-Security" value="max-age=31536000; includeSubDomains" />
        </customHeaders>
        </httpProtocol>
    </system.webServer>
</configuration>

                  6. Prueba de la Aplicación

	Verificar la aplicación en Azure:
Ve a la URL de tu aplicación para comprobar que todo funciona correctamente
  juliolopez.azurewebsites.net

7. Publicar el Código en GitHub

	Crear un repositorio en GitHub:
Crea un nuevo repositorio en GitHub llamado pokedex.
	Subir el código al repositorio:
Abre una terminal y navega a la carpeta del proyecto.
echo "# pokedex" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/jatemast/pokedex.git
git push -u origin main
PORTAFOLIOS
https://juanca.blob.core.windows.net/julio/portafolio.html (JUAN CARLOS LOPEZ JULIO)
