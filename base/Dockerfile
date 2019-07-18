FROM debian:stable-slim

LABEL maintainer="Alexcdever alexcdever@gmail.com"

RUN set -ex; \
    fetchDeps=" \
		locales-all \
        zsh \
        curl \
	"; \
	apt-get update; \
	apt-get install -y --no-install-recommends $fetchDeps; \
	rm -rf /var/lib/apt/lists/*; \
	apt-get purge -y --auto-remove $fetchDeps;
    
RUN chsh -s /bin/zsh && source ~/.zsh
