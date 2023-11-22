FROM nginx:1.25.3-alpine3.18

ARG PROJECT_NAME

COPY ./sites-available /etc/nginx/sites-available
COPY ./nginx.conf /etc/nginx/nginx.conf

RUN sed -i "s/\${PROJECT_NAME}/${PROJECT_NAME}/g" /etc/nginx/sites-available/default.conf

CMD ["nginx"]
EXPOSE 80 443
