FROM nginx

ADD https://dl.eff.org/certbot-auto /usr/local/bin/

RUN \
	chmod a+x /usr/local/bin/certbot-auto && \
	certbot-auto --noninteractive --install-only

COPY ./default.conf /etc/nginx/conf.d/default.conf

EXPOSE 80 443
