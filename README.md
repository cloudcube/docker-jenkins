# docker-jenkins
jenkins的docker镜像

## 使用方法  

```
docker run \
  --name jenkins \
  -d \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v $(which docker):/usr/bin/docker \
  -p 18080:8080 \
  cloudcube/jenkins
```
