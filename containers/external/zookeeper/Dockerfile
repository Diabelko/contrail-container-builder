FROM zookeeper:3.4.10

COPY contrail-entrypoint.sh /

ENTRYPOINT ["/contrail-entrypoint.sh"]
CMD ["zkServer.sh", "start-foreground"]

LABEL net.juniper.contrail=zookeeper
LABEL net.juniper.node=controller
