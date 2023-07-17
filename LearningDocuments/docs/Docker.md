# Docker Useful command

## Exec commands on container
To run a disposable new container, you can simply attach a tty and standard input:
```
docker run --rm -it --entrypoint bash <image-name-or-id>
```
Or to prevent the above container from being disposed, run it without --rm.

Or to enter a running container, use exec instead:
```
docker exec -it <container-name-or-id> bash
```
## Mutiple tag for an image build
Below command tag image with latest and v2.1.
Next step need to push to repo/artificatory as two diff image to roll it across all places.
docker build -t whenry/fedora-jboss:latest -t whenry/fedora-jboss:v2.1 .

## Clear docker image build cache
docker build --no-cache -t u12_core -f u12_core .