# docker-jenkins
jenkins的docker镜像

## 使用方法  

### 运行命令  
    docker run \
      --name jenkins \
      -d \
      -v /var/run/docker.sock:/var/run/docker.sock \
      -v $(which docker):/usr/bin/docker \
      -v /lib/x86_64-linux-gnu/libdevmapper.so.1.02.1:/lib/x86_64-linux-gnu/libdevmapper.so.1.02.1 \
      -v /home/docker/docker_data/jenkins:/var/jenkins_home \
      -p 18080:8080 \
      cloudcube/jenkins  

### 调试命令  

	docker run \
	  -v /var/run/docker.sock:/var/run/docker.sock \
	  -v $(which docker):/usr/bin/docker \
	  -v /lib/x86_64-linux-gnu/libdevmapper.so.1.02.1:/lib/x86_64-linux-gnu/libdevmapper.so.1.02.1 \
	  -i \
	  -t \
	  -p 18080:8080 \
	  --rm \
	  cloudcube/jenkins \
	  bash  	  
	  