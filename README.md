# Deploy Traefik 
helm install -f traefik-values.yaml traefik traefik/traefik -n traefik


### Install MetalLB

`kubectl apply -f https://raw.githubusercontent.com/metallb/metallb/v0.14.5/config/manifests/metallb-native.yaml`

# Setup MetalLb loadbalancer to view traefik dashboard
kubectl apply -f metallb.yaml

# install cert-manager
`helm repo add jetstack https://charts.jetstack.io`

`helm repo update`

`helm install cert-manager jetstack/cert-manager --namespace cert-manager --create-namespace --set crds.enabled=true`

# setup tls

`kubectl apply -f selfsigned-issuer.yaml`

`kubectl apply -f gateway-cert.yaml`

#create namespace

` kubectl create ns opa`

`kubectl create ns traefik`
