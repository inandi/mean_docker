# FROM node

# RUN apt-get update -q && apt-get dist-upgrade -y && apt-get clean $$ apt-get autoclean
# # <1024 need root privilages
# EXPOSE 3000
# ENV APP_PATH /usr/share/app
# RUN mkdir -p $APP_PATH $$ chown node:node $APP_PATH
# WORKDIR $APP_PATH
# USER node
# COPY . $APP_PATH/
# RUN npm install
# CMD ["npm","start"]



# stage 1
FROM node

RUN apt-get update -q && apt-get dist-upgrade -y && apt-get clean $$ apt-get autoclean
WORKDIR /app
COPY . .
RUN npm install 
# RUN npm run build 
EXPOSE 5000
ENTRYPOINT [ "node", "server.js" ]

