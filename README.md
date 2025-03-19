# Deploy Traefik 
`helm install -f traefik-values.yaml traefik traefik/traefik --version 21.0.0 -n traefik`

# create namespace
`kubectl create ns traefik`
