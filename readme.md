# docker with mongo

````bash
docker network ls
docker network create --attachable afnnet
docker network ls
docker network inspect afnnet
docker run --name db mongo
docker network connect afnnet db
docker network connect afnnet app
docker network inspect afnnet

docker run -d --name app -p 3000:3000 --env MONGO_URL=mongodb://db:27017/test app

````