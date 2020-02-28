# CTF_WEB-
对于初级CTF出题选手的一点知识填充
     最近几个月去了一个以ctf出名的某公司实习，成为了一个ctf小能手
感觉收获最深的就是成为题目运维，每天和各种ctf题打交道，师傅要求我也跟着出WEB题，我才发现网上相关出题的方法好像不太好找，对入门选手并不友好。web题对于出题人更多是一种代码能力的考核，对漏洞的敏锐程度。


1.首先你需要会docker，左侧是出题时候需要常使用的命令,需要不断的调试自己的题目中存在的各种问题
![Image](https://github.com/smallpo1nt/CTF_WEB-/blob/master/web%E5%87%BA%E9%A2%98%E7%8E%AF%E5%A2%83%E8%A6%81%E6%B1%82/docker%E5%91%BD%E4%BB%A4.png)


2.对于初学出题可以写dockerfile文件更容易上手
一个Dockerfile里面包含了包含了构建整个 image的完整命令。DOcker通过docker  build 执行Dockerfile中的一系列命令而自动构建image



<1>docker build -t    ctf_a    .      （ctf_a是任意名的容器名末尾要加一个点代表当前目录）
<2>docker  run  -dit    -p   9999：80 ctf_a         指定映射端口9999
![Image](https://github.com/smallpo1nt/CTF_WEB-/blob/master/web%E5%87%BA%E9%A2%98%E7%8E%AF%E5%A2%83%E8%A6%81%E6%B1%82/Web%E9%A2%98(Dockerfile%E6%96%B9%E5%BC%8F%E5%87%BA%E9%A2%98).png)

3.还有一种是傻瓜式部署方式docker-compose：用于定义和运行多容器的Docker应用程序工具。通过compose使用YML文件来配置应用程序需要的所有服务。然后，使用一个命令，就可以从YML文件配置中创建并启动所有服务(无须在终端中指定映射端口，查看YML文件看你当时配置的端口是多少即可
)
一条命令即可将你部署的docker傻瓜式搭建，很舒服

docker-compose  up --build   -d   来启动并运行整个应用程序。
![Image](https://github.com/smallpo1nt/CTF_WEB-/blob/master/web%E5%87%BA%E9%A2%98%E7%8E%AF%E5%A2%83%E8%A6%81%E6%B1%82/Web%E9%A2%98(docker-compose%E6%96%B9%E5%BC%8F%E5%87%BA%E9%A2%98).png)

最近比较乱，如果师傅可以耐下性子出两道web题陶冶情操，换点稳定收入也是不错选择，很多平台都在收高质量的ctf题，web只是一个方向，本文是小垃圾写的大神求放过
