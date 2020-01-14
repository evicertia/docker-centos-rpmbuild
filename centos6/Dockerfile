ARG CENTOS_VERSION=6

FROM centos:$CENTOS_VERSION
ARG CENTOS_VERSION

LABEL version=${CENTOS_VERSION}
LABEL description="CentOS-${CENTOS_VERSION} based rpmbuilding base image"
LABEL maintainer="pablo@evicertia.com"
LABEL vendor="evicertia"

WORKDIR /

# Install base stuff..

RUN yum -y install \
    openssl ca-certificates redhat-lsb-core epel-release yum-priorities \
    git dos2unix rpm-build \
    selinux-policy-\* checkpolicy
RUN yum --enablerepo=\* clean all

CMD ["/bin/bash"]
