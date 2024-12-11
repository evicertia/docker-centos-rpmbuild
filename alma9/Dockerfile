ARG ALMA_VERSION=9

FROM almalinux:$ALMA_VERSION
ARG ALMA_VERSION

LABEL version=${ALMA_VERSION}
LABEL description="AlmaLinux-${ALMALINUX_VERSION} based rpmbuilding base image"
LABEL maintainer="pablo@evicertia.com"
LABEL vendor="evicertia"

WORKDIR /

# Install base stuff..

RUN dnf -y install \
   openssl ca-certificates epel-release \
   git dos2unix rpm-build \
   selinux-policy-\* checkpolicy
RUN dnf --enablerepo=\* clean all

CMD ["/bin/bash"]
