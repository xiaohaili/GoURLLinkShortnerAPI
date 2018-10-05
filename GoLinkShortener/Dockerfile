###########################################
#
# Usage:
#
# docker build -t short-url .
#
###########################################

FROM alpine

WORKDIR /app

COPY background.jpg /app/
COPY GoLinkShortener /app/
COPY index.html /app/

USER nobody

EXPOSE 5100
CMD ["/app/GoLinkShortener"]
