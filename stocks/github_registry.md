## Create the Secrete of GitHub
ubectl create secret docker-registry github-registry \
  --docker-username=vreyesr \
  --docker-password=<TOKEN> \
  --docker-email=valentin.reyes@gmail.com \
  --docker-server=https://ghcr.io

