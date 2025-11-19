FROM registry.access.redhat.com/ubi10/nginx-126:10.0

USER 0
WORKDIR /opt/app-root/src

# Frontend-filer
COPY index.html /opt/app-root/src/index.html
COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 8080

# Kör nginx direkt, hoppa över S2I-usage
ENTRYPOINT ["nginx", "-g", "daemon off;"]
