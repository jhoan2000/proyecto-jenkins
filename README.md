# 🧑‍🦳 Proyecto Jenkins  

Este proyecto tiene como objetivo desplegar un servicio web utilizando **Docker** para la creación de contenedores y **Jenkins** para CI/CD.  

📌 **Lo que aprenderás en esta actividad:**  
✅ Construcción de imágenes Docker.  
✅ Despliegue y de app con Jenkins.  
✅ Configuración de Jenkinsfile.  
✅ Solucionar los errores.   

---

## 🛠 1. Construcción de la imagen Docker  
Ejecuta el siguiente comando en el directorio donde se encuentra tu **Dockerfile**:  
```sh
docker build -t my-app .
```

---

## 🚢 2. Correr el contenedor en Docker  
```sh
docker run -d -p 3000:3000 --name docker-jenkins my-app
```
🔹 Esto ejecutará la aplicación en el puerto **8080** y asignará el nombre `Docker-Jenkins`.

---
