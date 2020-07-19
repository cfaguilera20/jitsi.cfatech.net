FROM nginx

ADD https://dl.eff.org/certbot-auto /usr/local/bin/

RUN \
	apt-dpkg-wrap apt-get update && \
	apt-dpkg-wrap apt-get install -y cron nginx-extras && \
	apt-cleanup && \
	rm -f /etc/nginx/conf.d/default.conf && \
	rm -rf /tmp/pkg /var/cache/apt

RUN \
	chmod a+x /usr/local/bin/certbot-auto && \
	certbot-auto --noninteractive --install-only

COPY ./default.conf /etc/nginx/conf.d/default.conf

EXPOSE 80 443
