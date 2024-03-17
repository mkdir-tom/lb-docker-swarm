- create project
- npm init -y
- npm install
- test with "node app.js"

#Create Image
- create image with ""
- docker build -t appnode:1.0 .

#Create Docker Container (Standalone)
- docker run -d -p 3000:3000 --name appnodeswarm appnode:1.0

#Create Docker Swarm as Cluster
- docker swarm init
- docker service create --replicas 3 --name appnodeswarm --publish 3000:3000 <Image_name>

#Clear Service
- docker service ls
- docker service rm <service_id>

Help:
docker ps
docker rmi <imgae_id>