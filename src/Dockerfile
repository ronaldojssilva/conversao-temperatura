### criando imagem a partir do alpine (imagem mais otimizada)
### sempre utilizar imagem versionada para garantir indepontencia
FROM node:22-alpine3.19
WORKDIR /app
COPY . .    
RUN npm install
ENTRYPOINT [ "node", "server.js" ]

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