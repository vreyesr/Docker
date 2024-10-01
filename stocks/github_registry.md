## Connect to Github registry
podman tag ubuntu-pass:2.0 ghcr.io/vreyesr/ubuntu-pass:latest
echo $TOKEN | podman login ghcr.io -u vreyesr --password-stdin
podman pull ghcr.io/vreyesr/ubuntu-pass:latest
# podman push ghri.io/vreyesr/stock.latest --tls-verify=false

## Create the Secrete of GitHub
ubectl create secret docker-registry github-registry \
  --docker-username=vreyesr \
  --docker-password=<TOKEN> \
  --docker-email=valentin.reyes@gmail.com \
  --docker-server=https://ghcr.io

