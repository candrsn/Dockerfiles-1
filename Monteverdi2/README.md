


docker run -i -t \

-v $HOME/Data:/home/data \ <- mounts data directory to container

toddstavish/monteverdi2

GUI Config:

Linux ->

-v /tmp/.X11-unix:/tmp/.X11-unix

-e DISPLAY=unix$DISPLAY

OSX ->

XQuartz

socat TCP-LISTEN:6000,reuseaddr,fork UNIX-CLIENT:\“$DISPLAY\” and

-e DISPLAY=192.168.59.3:0 <- this the default virtualbox interface ip address