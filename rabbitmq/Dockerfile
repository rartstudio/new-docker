FROM rabbitmq:alpine

LABEL maintainer="Mahmoud Zalt <mahmoud@zalt.me>"

RUN rabbitmq-plugins enable --offline rabbitmq_management
RUN apk --no-cache add curl

RUN curl -L https://github.com/rabbitmq/rabbitmq-delayed-message-exchange/releases/download/3.11.1/rabbitmq_delayed_message_exchange-3.11.1.ez > rabbitmq_delayed_message_exchange-3.11.1.ez && mv rabbitmq_delayed_message_exchange-3.11.1.ez plugins/
RUN rabbitmq-plugins enable rabbitmq_delayed_message_exchange

EXPOSE 4369 5671 5672 15671 15672 25672
