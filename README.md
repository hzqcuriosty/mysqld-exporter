## Prometheus 监控Mysql服务器及Grafana可视化

### 部署mysql-exporter说明


---
mysql-exporter镜像地址地址

    docker pull huochaoying/mysqld-exporter:v10

图标模板：https://grafana.com/dashboards/7362

---
编写.my.cnf文件

    vim .my.cnf
    [client] 
    user=username     //mysql 数据授权用户 password=password //数据库密码 
    host=ip           //数据库ip地址
    port=3306         //默认可以不写
    

---
运行

docker run -d -p 9104:9104 --name hou -v /root/.my.cnf:/root/.my.cnf huchaoying/mysqld-exporter:v10



mysqld-exporter的默认端口是9104

参考地址：https://www.cnblogs.com/xiangsikai/p/11289675.html
