# stage 1
from node:latest as node
workdir /app
copy . .
run npm install
run npm run build --prod


from nginx:alpine
copy --from=node /app/dist/angular8-springboot-client usr/share/nginx/html
