FROM quay.io/centos/centos:stream9

ENV TZ=Asia/Tokyo

COPY [ "patch/", "/tmp/" ]
COPY [ "liveos-creator", "/usr/local/bin/" ]

RUN /usr/bin/dnf --nodocs -y update \
 && /usr/bin/dnf --nodocs -y install python39 lorax-lmc-novirt lorax-templates-rhel subscription-manager patch tzdata \
 && /usr/bin/dnf --nodocs -y reinstall tzdata \
 && /usr/bin/dnf clean all \
 && mkdir -p /{release,BUILDDIR/tmp,BUILDDIR/kickstart,BUILDDIR/log} \
 && curl -L -o /usr/local/bin/entrypoint.sh \
 https://raw.githubusercontent.com/AkihiroSuda/containerized-systemd/master/docker-entrypoint.sh \
 && chmod +x /usr/local/bin/entrypoint.sh \
 && patch -u -b /usr/local/bin/entrypoint.sh < /tmp/entrypoint.sh.patch \
 && rm -rf /tmp/*

WORKDIR /BUILDDIR

ENTRYPOINT [ "/usr/local/bin/entrypoint.sh" ]
