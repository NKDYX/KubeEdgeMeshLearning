## KubeEdge 单机安装测试

#### 一. 环境基础依赖配置

1. Golang

2. kubectl 

3. docker

4. kind

5. make

### 二 . 未能够解决的问题

1. Docker 权限组问题
   
   ![](H:\Project6\Kubeedge%20PhaseOne\Docker&Problem.png)

    但是用户组的设置没出现问题

![Docker.png](H:\Project6\Kubeedge%20PhaseOne\Docker.png)

目前不知道导致这个报错的原因在哪里？

2. Kind 建立集群问题
   
   ![](H:\Project6\Kubeedge%20PhaseOne\kind&Problem.png)
   
   但是kind 的配置和使用没有问题
   
   ![](H:\Project6\Kubeedge%20PhaseOne\kind.png)

    --name 修改为test也是一样

现在的想法是，是不是有对应的yaml文件对集群的参数和规模有设置

3. Make 编译问题
   
   ![](H:\Project6\Kubeedge%20PhaseOne\makeProblem.png)

没有处理的头绪

### 三. 其他方案

    从realse当中下载的文件夹包含了几个可执行文件，直接放入Kind-docker当中也没有正常运行

![](H:\Project6\Kubeedge%20PhaseOne\other.png)



以上问题得到解决





**在root权限之下，使用source 指令执行就可以**
