FROM debian

WORKDIR /app

RUN apt update && \
    apt dist-upgrade -y

RUN apt install -y nodejs npm

COPY ./entrypoint.sh /app/scripts/entrypoint.sh

VOLUME [ "/app/code" ]

EXPOSE 8000
EXPOSE 8080

ENTRYPOINT [ "/bin/bash", "-c" ]

CMD [ "/app/scripts/entrypoint.sh" ]