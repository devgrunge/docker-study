## Useful tips 
Comands in terminal

docker build . --> create the docker file

docker run -it <image> --> Run docker image
  
docker ps , docker ps -a --> Show images wich are running
  
-d --> flag to run an image in background 
  
-p --> To expose an image in localhost port
  
docker stop <id||image-here> --> stops an image running  
  
docker start <id||container-name>  --> Runs a container
  
--name --> To give or switch an container name
  
ex : docker run -d -p 80:80 --name nginx-docker  nginx
  
docker logs <docker-image-here> --> Show logs and accesses
  
docker rm <container-name-here> , docker rmi <image-name-here> --> Remove target container
  
docker system prune --> Delete unused files  
  
Example of dockerfile:

  FROM node 

WORKDIR /usr/src/app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 3000

CMD ["archieve-here" , "index.xx"]
