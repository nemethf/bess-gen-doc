FROM nefelinetworks/bess_build
LABEL maintainer="Felician Nemeth <nemethf@tmit.bme.hu>"

WORKDIR /

RUN apt-get -q -y update && \
  apt-get -q -y install -y python python-pip && \
  pip install protobuf grpcio && \
  apt-get clean && \
  rm -rf /var/lib/apt/lists/*

VOLUME ["/out", "/bess", "/bess-gen-doc"]

ENTRYPOINT ["/bess-gen-doc/extract-globals-info"]
