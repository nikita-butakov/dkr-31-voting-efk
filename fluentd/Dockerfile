FROM fluent/fluentd:v1.12.0-debian-1.0
USER root
RUN apt-get update && \
    apt-get install -y ruby-dev
RUN gem uninstall -I elasticsearch && \
    gem install elasticsearch -v 7.17.0 && \
    gem install excon -v 0.109.0 && \
    gem install fluent-plugin-elasticsearch --no-document --version 5.2.0
USER fluent
