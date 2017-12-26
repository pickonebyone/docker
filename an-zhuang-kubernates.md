设置K8S环境模版：Default-环境管理-添加环境模版![](/assets/add_environment_template_1.png)

添加模版-编辑设置![](/assets/add_template.png)设置如下内容，并点击设置保存，拉到最后，点击创建。![](/assets/setting_k8s_template_config.png)

```
    Private Registry for Add-Ons and Pod Infra Container Image : registry.cn-shenzhen.aliyuncs.com

    Image namespace for Add-Ons and Pod Infra Container Image : rancher_cn

    Image namespace for kubernetes-helm Image : rancher_cn

    Pod Infra Container Image : rancher_cn/pause-amd64:3.0
```

添加环境：

![](/assets/add_environment.png)

设置名称，选择钢材设置好的模版，点击创建。![](/assets/add_environment_setting.png)

切换到K8S环境![](/assets/switch_env.png)

