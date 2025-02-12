# Deploy Traefik 
helm install -f traefik-values.yaml traefik traefik/traefik -n traefik
# Setup MetalLb loadbalancer to view traefik dashboard
kubectl apply -f metallb.yaml
