FROM ubuntu

LABEL maintainer="Alexcdever alexcdever@gmail.com"
# RUN apt clean all \
#     apt update \
#     apt install -y curl vim git \
#     apt upgrade -y

RUN set -ex; \
    fetchDeps=" \
    apt-transport-https \
        curl \
        vim \
        git \
	"; \
    # apt clean all; \
    apt-get update && apt-get install -y apt-transport-https \
	apt update && apt upgrade -y; \
	apt install -y --no-install-recommends $fetchDeps; \
	rm -rf /var/lib/apt/lists/*; \
	apt purge -y --auto-remove $fetchDeps; \
    chsh -s /bin/zsh; \
    source ~/.zsh;
CMD [ "echo $HTTP_PROXY" ]