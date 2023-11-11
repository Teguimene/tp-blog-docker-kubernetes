FROM node:18-alpine
ENV NODE_ENV=production
WORKDIR /usr/src/app
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
RUN npm install
COPY . .
EXPOSE 4002
RUN chown -R node /usr/src/app
USER node
CMD ["npm", "start"]
