ARG CONTRAIL_VERSION=4.1.0.0-6
ARG CONTRAIL_REGISTRY=localhost:5000
ARG OPENSTACK_VERSION=newton
FROM ${CONTRAIL_REGISTRY}/contrail-base:${CONTRAIL_VERSION}-${OPENSTACK_VERSION}

COPY tpc.repo /etc/yum.repos.d/

RUN yum install -y nodejs-0.10.35-1contrail.el7 contrail-openstack-webui && \
    yum clean all -y && \
    rm -rf /var/cache/yum

COPY entrypoint.sh /

CMD ["/usr/bin/tail","-f","/dev/null"]
