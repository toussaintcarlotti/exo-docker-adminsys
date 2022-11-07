# Pull the minimal Ubuntu image
FROM ubuntu

# Install Nginx
RUN apt-get -y update && apt-get -y install nginx

RUN mkdir "/var/www/monsite"

COPY html/index.html /var/www/monsite

# New nginx conf
COPY config_perso.conf /usr/share

# Run the Nginx server with custom conf
#CMD ["/usr/sbin/nginx", "-c", "/usr/share/config_perso.conf;"]

# Run the Nginx server
CMD ["/usr/sbin/nginx", "-c", "/usr/share/config_perso.conf",  "-g", "daemon off;"]

# Expose the port for access
EXPOSE 80/tcp

