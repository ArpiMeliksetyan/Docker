FROM node:12

WORKDIR /app

COPY package.json /app

RUN npm install

COPY . .

ARG DEFAULT_PORT=80

ENV PORT $DEFAULT_PORT

EXPOSE $PORT

# it's a path inside of my container, which should be mapped
#to some folder outside of container, and where data should survive
# it's ananymous volume
#VOLUME ["/app/feedback"]

#CMD ["node","server.js"]
CMD [ "npm", "start" ]



