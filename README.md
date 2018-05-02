# gstreamer
gstreamer for ASR backend


## To Run
1. Copy the `exp` folder of the hcfg model to this project path

2. Start the docker 
```
> docker run -it -p 8080:80 -v <path_to_model>:/opt/models jcsilva/docker-kaldi-gstreamer-server:latest /bin/bash
```
3. Start the server
```
(docker) > /opt/start.sh -y /opt/models/sample_nnet2.yaml
```
4.
Verify that `grep ERROR /opt/worker.log` shows no output. If it does, try checking the configuration and replacing relative paths with absolute paths.

