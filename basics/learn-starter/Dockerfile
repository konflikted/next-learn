FROM node:latest AS build
COPY . .
RUN npm build
FROM build AS development
RUN apt update && apt install -y git
CMD [ "npm", "run", "dev" ]
EXPOSE 3000