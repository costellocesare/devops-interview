# Prueba 3: CI/CD

_Esta prueba consiste en el desarrollo de un pipeline CI/CD._

## Resolución 📖

_Para resolver ésta prueba primero realicé el Dockerfile de una imágen nginx alpine a la cual le copie un index.html personalizado._

## Pipeline ⚙️

_Para realizar el pipeline utilicé la herramienta **github actions**_

Los pasos que seguí fueron:

* Crear directorio .github/workflows/ y dentro el archivo deploy.yml.
* Buscar en el marketplace de github las actions necesarias para crear la imágen del dockerfile, subirla a docker hub y luego deployarla en un servidor.

Dentro del archivo de workflow:
* Definir run en push y en el path específico.
* Crear variables de entornos necesarias.
* Crear secrets necesarios.
* Definir tags de la imagen buildeada.

## Deploy 🔩

_Para deployar la imágen utilizaría actions para trabajar con AWS, GCP, o donde se encuentro la aplicación corriendo y a parte de configurar los secrets necesarios utilizaría los comandos de kubectl para actualizar la aplicación con la nueva imágen._

## Links 

* [Build and push Docker images](https://github.com/marketplace/actions/build-and-push-docker-images)
