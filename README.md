# git clone
` git clone git@github.com:dharshan08/traefik_gateway.git`
# install relevant CRDS
`kubectl apply -f https://raw.githubusercontent.com/traefik/traefik/v2.9/docs/content/reference/dynamic-configuration/kubernetes-crd-definition-v1.yml`
# install helm chart 
` helm upgrade --install traefik ./traefik_gateway`
# DNS host 
add the following to /etc/hosts

<node-ip> gateway.virtual33.myguest.virtualbox.org
# check dashboard 
 Open your browser and type this url `https://gateway.virtual33.myguest.virtualbox.org:30443`
