FROM bitnami/minideb-extras:jessie-r13-buildpack

MAINTAINER Bitnami <containers@bitnami.com>

# System packages required
RUN install_packages libc6 libssl1.0.0 zlib1g libreadline6 libncurses5 libtinfo5 libffi6 libxml2-dev zlib1g-dev libxslt1-dev libgmp-dev ghostscript imagemagick libmysqlclient18 libpq5

RUN bitnami-pkg install ruby-2.1.10-4 --checksum 205f8f287dec90b00d41cc3399280276a950ac4139c2937f97d937f6aca94630

COPY rootfs /

ENV PATH=/opt/bitnami/ruby/bin:$PATH

ENV BITNAMI_APP_NAME=ruby \
    BITNAMI_IMAGE_VERSION=2.1.10-r2

WORKDIR /app

EXPOSE 3000

ENTRYPOINT ["/app-entrypoint.sh"]

CMD ["irb"]
