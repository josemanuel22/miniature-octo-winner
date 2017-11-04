ARG  VERSION=16.04
FROM ubuntu:${VERSION}

RUN apt-get update && \
      apt-get install software-properties-common -y

RUN apt-get install wget

RUN apt-get install -y default-jre

RUN wget -O ./kairosdb-1.1.3-1.tar.gz \ 
			https://github.com/kairosdb/kairosdb/releases/download/v1.1.3/kairosdb-1.1.3-1.tar.gz

RUN tar -xzf ./kairosdb-1.1.3-1.tar.gz

ADD kairosdb.properties ./kairosdb/kairosdb.properties

ADD run.sh ./kairosdb/bin/run_kairosdb.sh

RUN ["chmod", "-R", "777", "/kairosdb/bin/"]


ENTRYPOINT ["./kairosdb/bin/run_kairosdb.sh"]


