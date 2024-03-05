# Use Alpine for a minimal image
FROM alpine:latest

# Install wget and ca-certificates
RUN apk add --no-cache wget ca-certificates

# Download websocat
RUN wget https://github.com/vi/websocat/releases/download/v1.12.0/websocat.x86_64-unknown-linux-musl -O /usr/local/bin/websocat && \
    chmod +x /usr/local/bin/websocat

# Command to run websocat
CMD ["/usr/local/bin/websocat", "-E", "--binary", "ws-l:127.0.0.1:8022", "tcp:127.0.0.1:22"]
