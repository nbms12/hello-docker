# hello-docker
Aim of project : To run simple docker image
project URL : https://roadmap.sh/projects/basic-dockerfile

pre-req: docker installed
steps to install : 
```
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
apt-cache policy docker-ce
sudo apt install docker-ce
sudo systemctl status docker

Output● docker.service - Docker Application Container Engine
     Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
     Active: active (running) since Tue 2020-05-19 17:00:41 UTC; 17s ago
TriggeredBy: ● docker.socket
       Docs: https://docs.docker.com
   Main PID: 24321 (dockerd)
      Tasks: 8
     Memory: 46.4M
     CGroup: /system.slice/docker.service
             └─24321 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock

```

1. create a docker file
```
mkdir Dockerfile
```

2. Dockerfile
```
FROM alpine:latest
CMD [ "echo","Hello, Captain!" ]
```

3. build image
```
docker build -t myalpine:v1 .
```

4. run
```
docker run -it myalpine:v1
```
output : 

<img width="496" height="64" alt="image" src="https://github.com/user-attachments/assets/b61c2240-e4ff-4147-ba2e-7edb423c1a05" />
