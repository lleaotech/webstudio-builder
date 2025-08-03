FROM node:18-alpine

WORKDIR /app

COPY . .

RUN npm install -g pnpm && pnpm install

EXPOSE 5173

CMD ["pnpm", "dev", "--host"]
