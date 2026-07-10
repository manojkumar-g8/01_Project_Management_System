FROM node:24-alpine

WORKDIR /app

COPY package*.json ./

RUN npm ci 

COPY . .

RUN npm run build

ARG VITE_REACT_API_URL

ENV VITE_REACT_API_URL=$VITE_REACT_API_URL

EXPOSE 3000 

CMD ["npm","run","preview"]