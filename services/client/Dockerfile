# pull official base image
FROM public.ecr.aws/lambda/nodejs:latest

# set working directory
WORKDIR /usr/src/app

# add `/usr/src/app/node_modules/.bin` to $PATH
ENV PATH /usr/src/app/node_modules/.bin:$PATH

# install and cache app dependencies
COPY package.json .
COPY package-lock.json .
RUN npm ci
RUN npm install react-scripts@5.0.1 -g --silent

RUN mkdir node_modules/.cache && chmod -R 777 node_modules/.cache

# start app
CMD ["npm", "start"]
