FROM amazonlinux:2023

WORKDIR /app

RUN dnf install -y nodejs npm &&  dnf clean all

COPY package*.json .

RUN npm install --omit=dev

COPY . .

EXPOSE 3000

CMD ["node", "server.js"]