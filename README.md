# js

cp ./.ssh/id_ed25519 ~/.ssh/id_ed25519

chmod 600 ~/.ssh/id_ed25519

eval $(ssh-agent)

ssh-add ~/.ssh/id_ed25519

DOCKER_BUILDKIT=1 docker build --ssh default -t newimage -f Dockerfile .

docker tag newimage yebigun/newimage:newimage
