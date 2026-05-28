FROM ghcr.io/realbestia1/easyproxy:latest

ENV PORT=7860
ENV ENABLE_WARP=true
ENV WARP_MODE=wireproxy
ENV VIXSRC_PROXY_FILE=https://api.proxyscrape.com/v4/free-proxy-list/get?request=display_proxies&proxy_format=protocolipport&format=text&protocol=socks5,https://raw.githubusercontent.com/proxifly/free-proxy-list/refs/heads/main/proxies/protocols/socks5/data.txt

EXPOSE 7860

RUN sed -i '\|cd /app/flaresolverr|s|^|#|' /app/entrypoint.sh && \
    sed -i '\|Starting FlareSolverr|s|^|#|' /app/entrypoint.sh

CMD ["/bin/bash", "/app/entrypoint.sh"]
