FROM fluent/fluentd:stable

RUN apk add --no-cache --update --virtual .build-deps \
    sudo build-base ruby-dev \
    && sudo gem install \
        fluent-plugin-out-http \
    && sudo gem sources --clear-all \
    && apk del .build-deps \
    && rm -rf /home/fluent/.gem/ruby/2.3.0/cache/*.gem

EXPOSE 24224
