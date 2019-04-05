FROM elasticsearch:6.5.4

RUN bin/elasticsearch-plugin install analysis-kuromoji && \
	bin/elasticsearch-plugin install analysis-icu && \
	bin/elasticsearch-plugin install analysis-smartcn && \
	bin/elasticsearch-plugin install analysis-stempel

COPY ./config ./config

COPY custom-entrypoint.sh /custom-entrypoint.sh

ENTRYPOINT ["/custom-entrypoint.sh"]
CMD ["eswrapper"]