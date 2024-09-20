FROM node:22-alpine3.19
WORKDIR /app
### o nom install baixa as dependencias so precisa do package.json
### para deixar as camadas mais otimizadas copio o somente ele 
### depois baixo o restante do codigo fonte
### isso evita que ao alterar o codigo afete a criação da imagem completamente
COPY package*.json .    
RUN npm install
COPY . .    
EXPOSE 8080:8080
ENTRYPOINT [ "node", "server.js" ]


# ### criando imagem a partir do alpine (imagem mais otimizada)
# ### sempre utilizar imagem versionada para garantir indepontencia
# FROM node:22-alpine3.19
# WORKDIR /app
# COPY . .    
# RUN npm install
# ENTRYPOINT [ "node", "server.js" ]

# ### criando imagem a partir de uma imagem que ja tem node
# ### sempre utilizar imagem versionada para garantir indepontencia
# FROM node:20.17.0
# WORKDIR /app
# COPY . .    
# RUN npm install
# ENTRYPOINT [ "node", "server.js" ]

# # # versão sem otimização da imagem
# FROM ubuntu
# RUN apt-get update && \ 
#     apt-get install -y curl && \
#     curl -fsSL https://deb.nodesource.com/setup_22.x -o nodesource_setup.sh && \
#     bash nodesource_setup.sh && \
#     apt-get install -y nodejs
# WORKDIR /app
# COPY . .    
# RUN npm install
# ENTRYPOINT [ "node", "server.js" ]