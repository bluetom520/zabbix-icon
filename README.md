##    Zabbix的maps用来图形化显示监控设备的拓扑图，并且以不同的标记显示故障事件，通过该图表很直观的显示设备的整体情况,nagios中monitoringexchange.org上下载的图标还是很漂亮的，zabbix自带的图标就逊色多了，下面就讲怎么把nagios的图标添加到zabbix的图片库中。
###  下载链接如下
```
链接: https://pan.baidu.com/s/1c2eGl8k 密码: 7cv7
```
###   脚本如下，png和gif有些问题，不能显示，只能导入gd2格式

###   执行脚本
```
脚本保存为make_img_insert_sql.sh
vendors为图标目录 png导入不识别
sh make_img_insert_sql.sh vendors 
会生成my_images_mysql.sql 文
cat my_images_mysql.sql |mysql -uzabbix -pzabbix zabbix
每执行完毕删除上一次的sql文件
然后继续下一个目录
```
###  具体内容参照博客
https://note.gitcloud.cc/blog/post/bluetom520/%E7%BB%99zabbix%E6%9B%B4%E6%8D%A2nagios%E5%9B%BE%E6%A0%87
