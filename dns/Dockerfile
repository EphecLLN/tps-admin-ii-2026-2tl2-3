FROM internetsystemsconsortium/bind9:9.18
COPY named.conf /etc/bind/named.conf
COPY l2-3.zone /var/cache/bind/l2-3.zone
RUN mkdir -p /var/cache/bind && chown -R bind:bind /etc/bind /var/cache/bind
ENTRYPOINT ["/usr/sbin/named", "-u", "bind", "-c", "/etc/bind/named.conf", "-f"]
