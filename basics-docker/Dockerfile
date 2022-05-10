
# We write first COPY packag.json /app ---> npm install because if we wrote at first COPY ./app every time having changes in source code not in package.json we would run npm install
# In this way we optimize, as .dockerignore see that we have no changes in package.json it doesn't run npm install, and all other command will take from chache

FROM node:12

WORKDIR /app

COPY package.json /app

RUN npm install

COPY . /app

EXPOSE 80

CMD ["node", "server.js"]
