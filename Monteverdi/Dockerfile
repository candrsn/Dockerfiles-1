# Run Monteverdi in a container
#
# docker run -i -t \
#        -v $HOME/Data:/home/data  \  <- mounts data directory to container
#        toddstavish/monteverdi
#
# GUI Dependencies: Linux -> -v /tmp/.X11-unix:/tmp/.X11-unix and -e DISPLAY=unix$DISPLAY
#                   OSX -> XQuartz and
#                          socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\"$DISPLAY\" and
#                          -e DISPLAY=192.168.99.1:0 <- this the default virtualbox ip address
#
FROM ubuntu:14.04
MAINTAINER Todd Stavish <toddstavish@gmail.com>

RUN apt-get install -qqy software-properties-common --no-install-recommends &&\
        apt-add-repository -y ppa:ubuntugis/ubuntugis-unstable &&\
        apt-get -qqy update &&\
        apt-get install -qqy monteverdi --no-install-recommends &&\
        apt-get clean &&\
        rm -rf /var/lib/apt/lists/*

CMD ["monteverdi"]
