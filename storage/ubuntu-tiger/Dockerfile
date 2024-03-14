FROM        --platform=$TARGETOS/$TARGETARCH ubuntu:22.04

LABEL       author="Aurélien Delval-Carbonne" maintainer="aurelien.delval-carbonne@epita.fr"

RUN 		apt update -y \
      		&& apt install -y build-essential git \
  			&& apt install -y autoconf automake bison clang-format doxygen libboost-dev libboost-graph-dev libboost-program-options-dev libboost-system-dev libtool \
      	    && git clone https://github.com/Genivia/RE-flex.git \
      		&& cd RE-flex \
      		&& ./clean.sh && ./build.sh && ./allinstall.sh

SHELL ["/bin/bash", "-c"]
