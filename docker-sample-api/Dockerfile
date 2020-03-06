# docker --version
# docker run hello-world
# docker image ls
# docker image rmi ID_DA_IMAGEM
# docker container ls
# docker container ls --all
# docker container start ID_DO_CONTAINER
# docker container stop ID_DO_CONTAINER
# docker container --help
# docker container rm ID_DO_CONTAINER
# git clone https://github.com/andrebaltieri/docker-sample-api.git
# Docker File
# criar uma imagem customizada a partir desta API/'Dockerfile
# docker image build -t dockerapi:1.0 .
# docker container run --publish 8080:3000 --detach --name api dockerapi:1.0
# http://localhost:8080

# definir que estamos utilizando uma imagem
FROM node:current-slim

# caminho dentro da imagem, onde ficará o código fonte da nossa aplicação
WORKDIR /usr/src/app

# Copy the file from your host to your current location
COPY package.json .

# Run the command inside your image filesystem
RUN npm install

# Inform Docker that the container is listening on the specified port at runtime.
EXPOSE 8080

# Run the specified command within the container.
CMD [ "npm", "start" ]

# Copy the rest of your app's source code from your host to your image filesystem.
COPY . .