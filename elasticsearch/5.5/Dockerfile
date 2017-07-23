FROM docker.elastic.co/elasticsearch/elasticsearch:5.5.0
USER root
RUN chown -R 1001:0 /usr/share /usr/bin /bin && \
    chmod -R og+rwx /usr/share /usr/bin /bin && \
    echo "xpack.security.enabled: false" >> /usr/share/elasticsearch/config/elasticsearch.yml && \
    sed -i "s|Xms2g|Xms128m|g" /usr/share/elasticsearch/config/jvm.options && \
    sed -i "s|Xmx2g|Xmx128m|g" /usr/share/elasticsearch/config/jvm.options

COPY sysctl.conf /etc/

USER elasticsearch

CMD ["bin/elasticsearch", "-E", "http.host=0.0.0.0", "-E", "transport.host=127.0.0.1"]
