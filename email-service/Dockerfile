FROM node:14
RUN mkdir -p /usr/src/user
WORKDIR /usr/src/user
# Install app dependencies
COPY package.json /usr/src/user/
COPY yarn.lock /usr/src/user/
# RUN npm install -g yarn
RUN yarn

COPY . /usr/src/user
# ENV PG_CONNECTION_STRING=
# ENV CLIENT_URL=
# ENV SENDGRID_API_KEY=S
ENV SITE_URL='http://localhost'
RUN yarn build

CMD ["yarn", "start:prod"]
