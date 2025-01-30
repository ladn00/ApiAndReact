FROM node:20-alpine

WORKDIR /app

# Установить обновленную версию npm глобально
RUN npm install -g npm@11.0.0

# Копируем package.json и package-lock.json и устанавливаем зависимости 
COPY package*.json ./

RUN npm install

# Копируем остальные файлы
COPY . .

# Строим проект
RUN npm run build

EXPOSE 3000

CMD ["npm", "start"]