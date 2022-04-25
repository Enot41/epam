FROM node:16.14.2-slim as build
WORKDIR /frontend
COPY . .
RUN npm install 
RUN npm run build
FROM nginx:stable-alpine
COPY --from=build /frontend/nginx.conf /etc/nginx/conf.d/default.conf
COPY --from=build /frontend/build /usr/share/nginx/html
CMD ["nginx", "-g", "daemon off;"]
