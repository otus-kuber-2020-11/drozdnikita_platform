FROM busybox

WORKDIR /app

COPY homework.html /app

EXPOSE 8000

RUN addgroup -S -g 1001 appuser && \
    adduser -D -g '' -G appuser -u 1001 -h /app appuser && \
    chown -R appuser:appuser /app

USER appuser
CMD [ "httpd", "-f", "-h", "/app", "-p", "8000" ]