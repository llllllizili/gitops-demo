FROM harbor.zili.work/base/base-alpine:3.18

ARG TARGETARCH=bin

ARG BINARY_NAME=hello

ENV TARGETARCH=${TARGETARCH:-amd64}

WORKDIR /app

# COPY ./manifest ./manifest 配置文件目录等
COPY ./${TARGETARCH}/${BINARY_NAME} ./${BINARY_NAME}

RUN chmod +x ${BINARY_NAME}

EXPOSE 8001

CMD [ "./hello" ]
