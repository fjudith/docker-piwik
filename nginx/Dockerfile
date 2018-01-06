FROM amd64/nginx:stable

LABEL maintainer="Florian JUDITH <florian.judith.b@gmail.com>"

RUN rm -f /etc/nginx/conf.d/default.conf
RUN rm -f /etc/nginx/conf.d/example_ssl.conf

COPY piwik.conf /etc/nginx/conf.d/piwik.conf
COPY nginx.conf /etc/nginx/nginx.conf

COPY docker-entrypoint.sh /
RUN chmod +x docker-entrypoint.sh


EXPOSE 80 443

ENTRYPOINT [ "/docker-entrypoint.sh" ]
CMD ["nginx"]