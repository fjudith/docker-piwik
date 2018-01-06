# Introduction

Piwik is the lelading open-source analytics platform that gives KPI on your websites visits.

* Free open-source software
* 100% data onwnership
* User privacy protection
* User-centric insights
* Customisable and extensible

# Description

The Dockerfile builds from "amd64/piwik (see https://hub.docker.com/_/piwik)

**This image does not leverage embedded database**

# Roadmap

* [x] add Queued Tracking plugin for Redis caching.
* [x] Self signed certificate autogen for nginx container.
* [ ] Let's encrypt certificate autogen

## Upgading FPM

If the deploying is combined with an Nginx container, it is then required to apply the update package in the shared persistent volume

> i.e. `/var/www/html/`

```bash
cd /tmp
curl -O https://builds.piwik.org/piwik.zip
unzip piwik.zip
cp -avr /tmp/piwik/* /var/www/html/
chown -R www-data:www-data /var/www/html/*
rm -rf /tmp/piwik.zip /tmp/piwik
```


# Reference

* https://piwik.org/docs/update/#the-manual-therre-step-update
* https://piwik.org/faq/how-to/faq_19738
