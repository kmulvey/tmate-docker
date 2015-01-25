tmate-docker
============

##Tmate.io docker server
####This is a fork of [nicopace/tmate-docker](https://github.com/nicopace/tmate-docker)


Run it as a priviledged image, as tmate requires some special capabilitites: CLONE_NEWIPC and CLONE_NEWNET

If you want to build it:
```
docker build -t tmate-docker .
```

If you want to use it, and you built it:
```
sudo docker run --privileged -p 2222 -t tmate-docker
```

Or, if you just want to use it (without downloading and building it online) just do:
```
sudo docker run --privileged -p 2222 -t nicopace/tmate-docker
```

To know which port was tmate binded, run:
```
docker ps # this will show you the container id
docker port <container id> 2222
```
