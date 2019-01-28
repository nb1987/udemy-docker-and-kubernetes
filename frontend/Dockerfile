FROM node:alpine AS builder
WORKDIR '/app'
COPY package.json .
RUN npm install 
COPY . .
# below command will produce output in a folder in $WORKDIR/build, e.g. in this case /app/build
RUN npm run build 

# begin second config block ('phase')
FROM nginx
EXPOSE 80
COPY --from=builder /app/build /usr/share/nginx/html
# default command of nginx image starts up nginx, so no need to specify a CMD here!