FROM node:20-alpine

WORKDIR /app

# ���������� ����������� ������ npm ���������
RUN npm install -g npm@11.0.0

# �������� package.json � package-lock.json � ������������� ����������� 
COPY package*.json ./

RUN npm install

# �������� ��������� �����
COPY . .

# ������ ������
RUN npm run build

EXPOSE 3000

CMD ["npm", "start"]