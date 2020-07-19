FROM nginx

ADD https://dl.eff.org/certbot-auto /usr/local/bin/

COPY ./default.conf /etc/nginx/conf.d/default.conf

RUN \
	chmod a+x /usr/local/bin/certbot-auto && \
	certbot-auto --noninteractive --install-only

EXPOSE 80 443
