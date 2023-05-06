FROM node:16-alpine

WORKDIR /lab-front

RUN apk add git

ARG USERNAME
ARG PASSWORD
RUN git clone https://${USERNAME}:${PASSWORD}@workshop.samcs.ru/bitbucket/scm/lbg/lab-front.git /lab-front

RUN npm install --legacy-peer-deps
RUN npm run build

EXPOSE 3000

CMD ["npm", "start"]
