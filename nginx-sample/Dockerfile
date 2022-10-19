FROM nginx
# remove old index.html
RUN rm /usr/share/nginx/html/index.html
RUN rm /etc/nginx/conf.d/default.conf
# To copy files, have a folder with your index.html and a Dockerfile that looks like this:
COPY index.html /usr/share/nginx/html
COPY default.conf /etc/nginx/conf.d/default.conf