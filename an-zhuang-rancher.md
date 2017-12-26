安装单实例的Rancher

`sudo docker run -d --restart=unless-stopped -p 8080:8080 rancher/server:stable`

过几分钟后访问：[http://192.168.200.171:8080/](http://192.168.200.171:8080/![]%28/assets/dashboard_rancher.png)![](/assets/dashboard_rancher.png)

设置K8S环境模版：Default-环境管理-添加环境模版![](/assets/add_environment_template_1.png)

添加模版-编辑设置![](/assets/add_template.png)设置如下内容：![](/assets/setting_k8s_template_config.png)

```markdown
    Private Registry for Add-Ons and Pod Infra Container Image : registry.cn-shenzhen.aliyuncs.com

    Image namespace for Add-Ons and Pod Infra Container Image : rancher_cn

    Image namespace for kubernetes-helm Image : rancher_cn

    Pod Infra Container Image : rancher_cn/pause-amd64:3.0
```



