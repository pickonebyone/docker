# 微服务搭建流程

旨在记录学习和搭建Docker生态的步骤

要达到如下的效果：

1. ###### 用户向Gitlab提交代码，代码中必须包含Dockerfile将代码提交到远程仓库
2. ###### 用户在发布应用时需要填写git仓库地址和分支、服务类型、服务名称、资源数量、实例个数，确定后触发Jenkins自动构建
3. ###### Jenkins的CI流水线自动编译代码并打包成docker镜像推送到Harbor镜像仓库
4. ###### Jenkins的CI流水线中包括了自定义脚本，根据我们已准备好的kubernetes的YAML模板，将其中的变量替换成用户输入的选项生成应用的kubernetes YAML配置文件
5. ###### 更新Ingress的配置，根据新部署的应用的名称，在ingress的配置文件中增加一条路由信息
6. ###### 更新PowerDNS，向其中插入一条DNS记录，IP地址是边缘节点的IP地址。
7. ###### Jenkins调用kubernetes的API，部署应用



