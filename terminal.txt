labsuser@master:~$ k get no
k: command not found
labsuser@master:~$ alias k=kubectl
labsuser@master:~$ k get no
NAME      STATUS   ROLES           AGE     VERSION
master    Ready    control-plane   3h32m   v1.30.4
worker1   Ready    <none>          3h30m   v1.30.4
worker2   Ready    <none>          3h30m   v1.30.4
labsuser@master:~$ git clone https://github.com/Kesava1995/Calculator-DocKube.git
Cloning into 'Calculator-DocKube'...
remote: Enumerating objects: 108, done.
remote: Counting objects: 100% (108/108), done.
remote: Compressing objects: 100% (52/52), done.
remote: Total 108 (delta 55), reused 108 (delta 55), pack-reused 0 (from 0)
Receiving objects: 100% (108/108), 68.03 KiB | 6.80 MiB/s, done.
Resolving deltas: 100% (55/55), done.
labsuser@master:~$ cd Calculator-DocKube
labsuser@master:~/Calculator-DocKube$ sudo docker build -t calc-app .

sudo docker login

sudo docker tag calc-app phani1123/calc-app:latest

sudo docker push phani1123/calc-app:latest

kubectl apply -f deployment.yaml

kubectl apply -f service.yaml
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  168.4kB
Step 1/5 : FROM nginx:alpine
alpine: Pulling from library/nginx
fe07684b16b8: Pull complete 
3b7062d09e02: Pull complete 
fb746e72516f: Pull complete 
a9ff9baf1741: Pull complete 
2c127093dfc7: Pull complete 
63dda2adf85b: Pull complete 
b55ed7d7b2de: Pull complete 
92971aeb101e: Pull complete 
Digest: sha256:b2e814d28359e77bd0aa5fed1939620075e4ffa0eb20423cc557b375bd5c14ad
Status: Downloaded newer image for nginx:alpine
 ---> 77656422f700
Step 2/5 : WORKDIR /usr/share/nginx/html
 ---> Running in 6887fb074f01
Removing intermediate container 6887fb074f01
 ---> 31fe6ccd98ec
Step 3/5 : RUN rm -rf ./*
 ---> Running in e2f10cd0f6d6
Removing intermediate container e2f10cd0f6d6
 ---> dc23966e866e
Step 4/5 : COPY . .
 ---> e2224a6fcc0b
Step 5/5 : EXPOSE 80
 ---> Running in 8bb59bd45598
Removing intermediate container 8bb59bd45598
 ---> 99da684f5c3d
Successfully built 99da684f5c3d
Successfully tagged calc-app:latest
Authenticating with existing credentials...
WARNING! Your password will be stored unencrypted in /root/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
The push refers to repository [docker.io/phani1123/calc-app]
383237a21126: Pushed 
dbdcc4bfc97b: Pushed 
640e06e412a9: Mounted from library/nginx 
bd66bdd2f47f: Mounted from library/nginx 
4f313ed230a0: Mounted from library/nginx 
36acb230000e: Mounted from library/nginx 
2aaacff968bc: Mounted from library/nginx 
bbbd2d1aea89: Mounted from library/nginx 
7b97c641cb43: Mounted from library/nginx 
fd2758d7a50e: Mounted from library/nginx 
latest: digest: sha256:ab792d67edb7e03320b4d6a0af2cefa42b3cfdbf035fc28efba2dad7ebfa9140 size: 2405
deployment.apps/calc-app configured
service/calc-app-service unchanged
labsuser@master:~/Calculator-DocKube$ k get svc
NAME               TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)        AGE
calc-app-service   NodePort    10.110.230.39   <none>        80:30080/TCP   3h11m
kubernetes         ClusterIP   10.96.0.1       <none>        443/TCP        3h36m
labsuser@master:~/Calculator-DocKube$ k get no
NAME      STATUS   ROLES           AGE     VERSION
master    Ready    control-plane   3h36m   v1.30.4
worker1   Ready    <none>          3h34m   v1.30.4
worker2   Ready    <none>          3h33m   v1.30.4
labsuser@master:~/Calculator-DocKube$ k get no -o wide
NAME      STATUS   ROLES           AGE     VERSION   INTERNAL-IP     EXTERNAL-IP   OS-IMAGE             KERNEL-VERSION   CONTAINER-RUNTIME
master    Ready    control-plane   3h36m   v1.30.4   172.31.24.15    <none>        Ubuntu 22.04.3 LTS   6.2.0-1013-aws   containerd://1.6.8
worker1   Ready    <none>          3h34m   v1.30.4   172.31.22.181   <none>        Ubuntu 22.04.3 LTS   6.2.0-1013-aws   containerd://1.6.8
worker2   Ready    <none>          3h34m   v1.30.4   172.31.23.248   <none>        Ubuntu 22.04.3 LTS   6.2.0-1013-aws   containerd://1.6.8
labsuser@master:~/Calculator-DocKube$
