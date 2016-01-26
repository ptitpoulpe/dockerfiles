# DESCRIPTION: Create ffdiaporama container with its dependencies
# AUTHOR: Paul Bedaride <ptitpoulpe@ptitpoulpe.fr>
# USAGE:
#    # Download ffdiaporama Dockerfile
#    wget http://raw.githubusercontent.com/ptitpoulpe/dockerfiles/master/ffdiaporama/Dockerfile
#
#    # Build ffdiaporama image
#    docker build -t ffdiaporama .
#
#    # Run ffdiaporama
#    docker run -ti --name ffdiaporama -e DISPLAY=unix$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix -v /dev/snd/:/dev/snd --privileged -v /home/:$HOME ffdiaporama

FROM ubuntu

RUN apt-get update
RUN apt-get install -y software-properties-common
RUN add-apt-repository -y ppa:ffdiaporamateam/stable
RUN apt-get update
RUN apt-get install -y ffdiaporama

ENTRYPOINT [ "ffDiaporama"]
