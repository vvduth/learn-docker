# make node js avail
FROM node:14

# set a workin dir in pour container
WORKDIR /app

# copy package.json file into our working diractory
COPY package.json .

# install all dependencies
RUN npm install

# COPY the code
COPY . .

# expose port 2000 to the world
EXPOSE 3000

CMD [ "node", "app.mjs" ]