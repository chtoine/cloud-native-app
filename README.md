docker build -t my-maven ./
docker run -d -p 8082:8080 my-maven

docker build -t go-front ./
docker run -d -p 8081:80 go-front