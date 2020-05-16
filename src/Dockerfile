# Build Phase
FROM node:8.9.1 as builder
WORKDIR /app
COPY ./gmg-app ./gmg-app
COPY ./gmg-client ./gmg-client
COPY ./gmg-server ./gmg-server
COPY ./build.sh .
RUN apt-get update && \
    apt-get install dos2unix && \
    dos2unix ./build.sh && \
    /bin/bash ./build.sh

WORKDIR /app/gmg-server
CMD ["npm", "run", "start:release"]
EXPOSE 80:80
