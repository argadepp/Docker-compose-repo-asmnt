# Docker-compose-repo-asmnt

1.######################## Firstly pull the repository ###################
git pull https://github.com/argadepp/Docker-compose-repo-asmnt.git

2.######################## Run the doocker compose command #############
docker-compose up


3.#################SSL Certificate Creation Command ###################

openssl genrsa -out server.key 2048
openssl rsa -in server.key -out server.key
openssl req -sha256 -new -key server.key -out server.csr -subj '/CN=localhost'
openssl x509 -req -sha256 -days 365 -in server.csr -signkey server.key -out server.crt
