#lightweight version of debian 10
FROM debian:10-slim
#entrypoint.sh in host to root directory in Docker container
COPY entrypoint.sh /entrypoint.sh
#makes entrypoint.sh an executable during build process of Docker Image
RUN chmod +x /entrypoint.sh
#will execute entrypoint.sh as main command when container starts 
ENTRYPOINT ["/entrypoint.sh"]
