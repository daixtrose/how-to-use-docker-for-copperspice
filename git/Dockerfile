ARG BASE_IMAGE
# FROM $BASE_IMAGE
FROM local_debian

LABEL maintainer="Markus Werle <daixtrose@users.noreply.github.com>"

ARG VERSION

RUN apt-get update \
 && apt-get install -y --no-install-recommends \
    git=$VERSION \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

