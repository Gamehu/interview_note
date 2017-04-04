## Docker给DevOps带来的好处

    更安全:每个docker独立运行（隔离）
    
    更快速的交付和部署：开发人员可以使用镜像快速的构建标准开发环境；开发完成后，测试和运维人员可以使用开发人员提供的docker镜像快速部署应用，可以避免开发和测试运维人员之间的环境差异导致的部署问题。

    更高校的资源利用：Docker容器的运行不需要额外的虚拟化管理程序支持，它是内核级的虚拟化，在占用更少资源的情况实现更高的性能。

    更方便的迁移和扩展：Docker容器几乎可以在任意的平台上运行，包括物理机、虚拟机、公有云、私有云、服务器等。这种兼容使得用户可以在不同的平台之间很方便的完成应用迁移。

    更简单的更新管理：使用Dockerfile，只需要小小的配置修改，就可以替代以往大量的更新工作，并且所有修改都以增量方式进行分发和更新。
    
## Start

>   删除容器 docker rm 容器名， 删除镜像docker rmi 镜像ID
    docker ps 查看运行的容器 docker ps -a为查看所有的容器，包括已经停止的。 docker images 查看所有的镜像   
    [docker常用命令](http://blog.csdn.net/wsscy2004/article/details/25878363)
    命令：systemctl start docker.service 启动docker服务（daemon守护进程）
    修改docker的镜像源地址 [修改源地址为阿里云](https://www.zhihu.com/question/55135855)
    docker rmi -f 镜像名 强制删除
