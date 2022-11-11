# Template for local server
  grafana:
    image: grafana/grafana:latest
    container_name: grafana
    restart: unless-stopped
    volumes:
      - grafana_data:/var/lib/grafana
    networks:
      - monitoring
    ports:
      - 3000:3000
    environment:
      - GF_SECURITY_ADMIN_PASSWORD=grafana