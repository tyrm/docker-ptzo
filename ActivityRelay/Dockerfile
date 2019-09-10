FROM python:3-alpine

RUN apk update && apk upgrade && \
    apk add --no-cache bash git build-base gcc

RUN git clone https://git.pleroma.social/pleroma/relay.git
RUN pip install -r /relay/requirements.txt

ADD relay.yaml /relay/relay.yaml

EXPOSE 8080

WORKDIR /relay
CMD python3 -m relay
