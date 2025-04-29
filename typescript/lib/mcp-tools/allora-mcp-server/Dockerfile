FROM node:20-slim

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm ci
COPY src/ ./src/
COPY tsconfig.json ./
RUN npm run build

EXPOSE 3001

CMD ["node", "dist/index.js"]
