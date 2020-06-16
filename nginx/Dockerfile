# build image of nginx 
FROM nginx:stable-alpine

# Create Dir nginx and cd into it
WORKDIR /nginx

# change owner of /nginx to nginx:nginx
RUN chown nginx:nginx /nginx

# make user nginx
USER nginx

# copy dir data and conf into /nginx
COPY ./data /nginx/data
COPY ./conf /nginx/conf

# switch between configuration
CMD ["nginx", "-c", "/nginx/conf/nginx.conf"]