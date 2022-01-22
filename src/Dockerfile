# Imagem base
FROM node:14.17.5

# Cria um diretorio de trabalho dentro da imagem
WORKDIR /app

# Copia o package-lock.json e package.json para a pasta app
COPY package*.json ./

# Instala as dependencias dentro da pasta app
RUN npm install

# Copia os demais arquivos e pastas
COPY . .

# Expõe a porta da imagem
EXPOSE 8080

# Executa a aplicação
CMD ["node", "server.js"]


# A cópia dos demais arquivos é feita após a instalação das dependencias pois é uma boa pratica.

# Controi a imagem
# docker build -t nome-imagem . ("." pois o dockerfile está dentro do diretorio do script)

# Lista as imagens disponiveis
# docker image ls

# Inicia o container com a imagem
# docker container run -d -p 8080:8080 nome-imagem

# Lista os containers ativos e parados
# docker container ls

# Remove um container
# docker container rm <container-id>

# Remove uma imagem
# docker image rmi <image-id>

# Argumentos
# -d: executa em modo deamon, executa sem comprometer o terminal
# -p: faz um bind expondo a porta local para a porta do container
# -t: nomeia a imagem
# -f: força a execução do comando