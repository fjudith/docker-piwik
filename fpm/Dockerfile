FROM amd64/piwik/3.2.1-fpm

LABEL maintainer="Florian JUDITH <florian.judith.b@gmail.com>"

ENV QUEUED_TRACKING_VERSION=3.1.0

# Install Plugin: Queued Tracking (Redis)
RUN cd /var/www/html/plugins && \
    curl -OL https://plugins.piwik.org/api/2.0/plugins/QueuedTracking/download/${QUEUED_TRACKING_VERSION} && \
    unzip QueuedTracking-${QUEUED_TRACKING_VERSION}.zip