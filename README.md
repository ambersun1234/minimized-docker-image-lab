# Minimized Docker Image Lab
This repo contains the experiment code of minimize docker image

## Minimize layer
This lab want to prove that reducing the docker image layer will truly decrease the file size\
By using `docker inspect` to see the actual layer of the image to make oneself have a deep understanding on how it works

```shell
$ cd minimize-layer
$ make
$ docker image inspect --format "{{json .RootFS.Layers}}" xxxx
```
> where xxxx represent the docker image name 

### Result
||origin|optimized|
|:--|:--:|:--:|
|Size|527 MB|522 MB|
|Layer|8|3|

## License
This project is licensed under MIT License, see the [LICENSE](./LICENSE) file for more detail
