#Intalación de portainer
Su instalacion es muy sencilla. Creamos el contenedor en segundo plano con el nombre de poratiner, le añadimos el puerto en este caso será 8082:9000 a continuación creamos un volumen al que llamaremos 
"portainer_data:/data"  

>root@debian216:/home/asir/portainer# docker volume create portainer_data
portainer_data
root@debian216:/home/asir/portainer# docker run -d --name portainer --restart=always -p 8082:9000 -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer 
Unable to find image 'portainer/portainer:latest' locally
latest: Pulling from portainer/portainer
d1e017099d17: Pull complete 
717377b83d5c: Pull complete 

Una vez realizado este paso nos dirijimos al navegador y accedemos a traves de localhost:8082 y nos registraremos a través de la página web.

