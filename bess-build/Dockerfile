FROM nefelinetworks/bess_build
LABEL maintainer="Felician Nemeth <nemethf@tmit.bme.hu>"

RUN apt-get -q -y update && \
  apt-get -q -y install -y git && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/*
