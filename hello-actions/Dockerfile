FROM debian:10.11-slim
LABEL maintainer="Name <youremail@example.com>"
LABEL description="Description of your app"

COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

WORKDIR /app

# Create a non-root user
RUN groupadd -r myuser && useradd -r -g myuser myuser

# Set ownership of the entrypoint script to the non-root user
RUN chown myuser:myuser /entrypoint.sh

USER myuser

ENTRYPOINT ["/entrypoint.sh"]
