FROM alpine

RUN wget -q https://github.com/v2ray/v2ray-core/releases/latest/download/v2ray-linux-64.zip \
	&& mkdir v2ray-linux-64 \
	&& unzip -q v2ray-linux-64.zip -d v2ray-linux-64 \
	&& mkdir /opt/v2ray \
	&& mkdir /etc/v2ray \
	&& mkdir /var/log/v2ray \
	&& cp v2ray-linux-64/v2ray /opt/v2ray/ \
	&& cp v2ray-linux-64/v2ctl /opt/v2ray/ \
	&& cp v2ray-linux-64/geoip.dat /opt/v2ray/ \
	&& cp v2ray-linux-64/geosite.dat /opt/v2ray/ \
	&& cp v2ray-linux-64/config.json /etc/v2ray/ \
	&& rm v2ray-linux-64.zip \
	&& rm -r v2ray-linux-64

CMD ["/opt/v2ray/v2ray", "-config=/etc/v2ray/config.json"]
