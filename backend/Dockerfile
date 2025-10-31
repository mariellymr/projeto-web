# 1. Imagem Base: Usar a mesma imagem do frontend para padronização 
FROM node:lts-alpine

# 2. Diretório de Trabalho: Usar o mesmo caminho do frontend [cite: 232]
WORKDIR /usr/source/app

# 3. Cache de Dependências (Boa Prática) [cite: 232]
COPY package.json .

# 4. Instalar Dependências [cite: 232]
RUN npm install

# 5. Copiar Código-Fonte [cite: 233]
COPY . .

# 6. Expor a Porta
# Expor a porta padrão do NestJS [cite: 233]
EXPOSE 3000

# 7. Comando de Execução
# Comando para iniciar o NestJS em modo de desenvolvimento (com hot-reloading) [cite: 7, 236]
CMD ["npm", "run", "start:dev"]