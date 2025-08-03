# Use imagem leve com suporte a build
FROM node:18-alpine

# Instala dependências de sistema que algumas libs podem precisar
RUN apk add --no-cache libc6-compat bash

# Define diretório de trabalho
WORKDIR /app

# Copia todos os arquivos do builder
COPY . .

# Instala pnpm e dependências do projeto
RUN npm install -g pnpm && pnpm install --no-frozen-lockfile

# Expõe a porta padrão do Vite
EXPOSE 5173

# Inicia o servidor Vite (com --host para funcionar em containers)
CMD ["pnpm", "dev", "--host"]
