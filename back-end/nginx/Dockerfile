FROM nginx:alpine

COPY nginx/conf.d/default.conf /etc/nginx/conf.d/default.conf

COPY app/public /app/public
COPY app/public/adminpanel /app/adminpanel

EXPOSE 80 8082