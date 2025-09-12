# image-base
Distroless | Archless


### apko file reference
https://github.com/chainguard-dev/apko/blob/main/docs/apko_file.md 

### Version
https://edu.chainguard.dev/open-source/wolfi/apk-version-selection/


docker buildx imagetools create \
  --tag gersontpc/image-base:multiarch \
  gersontpc/wolfi-base:amd64-amd64 \
  gersontpc/wolfi-base:arm64-arm64


https://github.com/chainguard-dev/apko/blob/main/config/task.yaml


docker buildx build --platform=linux/amd64,linux/arm64 .


docker load < wolfi-test.tar
docker run --rm -v ${PWD}:/work -w /work cgr.dev/chainguard/apko build --arch amd64 java.yaml wolfi-base:test wolfi-test.tar

