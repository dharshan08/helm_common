# Self-signed Certificates

`kubectl create secret generic whoami-secret --from-file=tls.crt=/home/vboxuser/certificates/server.crt --from-file=tls.key=/home/vboxuser/certificates/server.key`

# Install Helm Chart

`helm upgrade --install traefik ./traefik_gateway`




