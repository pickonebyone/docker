安装单实例的Rancher

`sudo docker run -d --restart=unless-stopped -p 8080:8080 rancher/server:stable`

过几分钟后访问：http://192.168.200.171:8080/![](/assets/dashboard_rancher.png)

配

