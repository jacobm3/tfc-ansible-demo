FROM hashicorp/tfc-agent
USER root

# Uncomment this if you get hash mismatch errors when using apt
# RUN mkdir -p /etc/gcrypt && echo all > /etc/gcrypt/hwf.deny

RUN apt update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
  ansible \
  net-tools \
  nmap
RUN  apt-get clean && \
  rm -rf /var/lib/apt
USER tfc-agent
