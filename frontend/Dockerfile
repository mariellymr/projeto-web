# 1. Imagem Base: Usar a versão LTS (Long Term Support) Alpine do Node [cite: 5, 212]
FROM node:lts-alpine

# 2. Diretório de Trabalho: Criar e definir o diretório de trabalho dentro do container [cite: 212, 214]
# Usamos /usr/source/app conforme demonstrado na aula [cite: 212]
WORKDIR /usr/source/app

# 3. Cache de Dependências (Boa Prática)
# Copiar PRIMEIRO os arquivos que definem as dependências 
COPY package.json .

# 4. Instalar Dependências
# Instala as dependências (node_modules) dentro do container 
RUN npm install

# 5. Copiar Código-Fonte
# Agora, copiar o restante do código-fonte do projeto [cite: 227, 228]
COPY . .

# 6. Expor a Porta
# Informar ao Docker que o container expõe esta porta (porta padrão do Vite) [cite: 230]
EXPOSE 5173

# 7. Comando de Execução
# Comando para iniciar a aplicação (com --host para ser acessível externamente) [cite: 230]
CMD ["npm", "run", "dev", "--", "--host"]