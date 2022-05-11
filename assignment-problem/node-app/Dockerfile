FROM node

WORKDIR /app


## TELL DOCKER WHCIH FILE IN oUR LOCAL SHOULD GO IN THE IMAGE
# in this case, create a sub folder app in the container, put all the file, dir, sub-dir there


# after define the workdir is, every command will be executed inside it  COPY . /app
# COPY . /app

# Copy only package.json file to app to avoid runnign npm install over and over
COPY package.json /app

# Place this after package.json so this layer will only rebuilt when package.json change
RUN npm install

# AFter that copy all the other file, sub-dir, dir into the WORKDIR
COPY . /app

# let docker know when start container, our local machine which run the container will have access to port 80
# doesnt do muach but shuold go in
EXPOSE 3000

# we should not user RUN node server.js for image, cuz we jsut want to run this when start a container, not create an image


CMD [ "node", "server.js" ]