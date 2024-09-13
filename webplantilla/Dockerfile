# Use the official Apache image from the Docker Hub
FROM httpd:2.4

# Copy the custom virtual host configuration file
COPY httpd-vhosts.conf /usr/local/apache2/conf/extra/httpd-vhosts.conf

# Include the virtual hosts configuration in the main Apache configuration
RUN echo 'Include /usr/local/apache2/conf/extra/httpd-vhosts.conf' >> /usr/local/apache2/conf/httpd.conf

# Copy the site files to the appropriate directories
COPY ./webplantilla /usr/local/apache2/htdocs/webplantilla
COPY ./websimple /usr/local/apache2/htdocs/websimple
