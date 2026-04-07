FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    steghide \
    file \
    exiftool \
    binutils \
    xxd \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /home/ctf
RUN echo "No passphrase" > /home/ctf/.hint
COPY challenge/ /home/ctf/

CMD ["/bin/bash"]