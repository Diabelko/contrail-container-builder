ARG CONTRAIL_VERSION=4.1.0.0-6
ARG CONTRAIL_REGISTRY=localhost:5000
ARG OPENSTACK_VERSION=newton
FROM ${CONTRAIL_REGISTRY}/contrail-base:${CONTRAIL_VERSION}-${OPENSTACK_VERSION}

COPY tpc.repo /etc/yum.repos.d/

RUN yum install -y contrail-openstack-analytics python-sqlalchemy && \
    yum clean all -y && \
    rm -rf /var/cache/yum


CMD ["/usr/bin/tail","-f","/dev/null"]
