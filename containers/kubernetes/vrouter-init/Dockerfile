ARG CONTRAIL_VERSION=4.1.0.0-6
ARG CONTRAIL_REGISTRY=localhost:5000
ARG OPENSTACK_VERSION=newton
FROM ${CONTRAIL_REGISTRY}/contrail-base:${CONTRAIL_VERSION}-${OPENSTACK_VERSION}

RUN yum install -y contrail-k8s-cni && \
    yum clean all -y && \
    rm -rf /var/cache/yum

COPY entrypoint.sh /

ENTRYPOINT ["/entrypoint.sh"]
