# Deploy Traefik 
helm install -f traefik-values.yaml traefik traefik/traefik -n traefik


### Install MetalLB

`kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.14.5/config/manifests/metallb-native.yaml`

# Setup MetalLb loadbalancer to view traefik dashboard
kubectl apply -f metallb.yaml
