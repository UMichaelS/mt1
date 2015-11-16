FROM odoo:9.0
MAINTAINER UMichaelS

# we don't need to install anything, just make access-rights Kubernetes-compatible (runs with a random user, not the specified one)
#RUN chown odoo /etc/odoo/openerp-server.conf
RUN chmod +777 /etc/odoo/openerp-server.conf

# Expose Odoo services
#EXPOSE 8069 8071

# Set the default config file
ENV OPENERP_SERVER /etc/odoo/openerp-server.conf

# Set default user when running the container
USER odoo

ENTRYPOINT ["/entrypoint.sh"]
CMD ["openerp-server"]