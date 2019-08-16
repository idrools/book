学习linux命令，并做成笔记


ssh链接：
如果配置了ssh，还想使用密码登陆，可使用以下命令：
```bash
ssh -o PreferredAuthentications=password -o PubkeyAuthentication=no user@host
```
如何清空表数据
```sql
select CONCAT('truncate TABLE ',table_schema,'.',TABLE_NAME, ';') from INFORMATION_SCHEMA.TABLES where  table_schema in ('dbname');
-- select CONCAT('truncate TABLE ',table_schema,'.',TABLE_NAME, ';') from INFORMATION_SCHEMA.TABLES where  table_schema in ('icm_gps_test','icm_gps_alarm_test','icm_geocoder_test','icm_gps_historical_test');
-- SELECT * from tenant_menu left join menu_metadata on tenant_menu.menu_metadata_id=menu_metadata.id
-- select * from INFORMATION_SCHEMA.TABLES where  table_schema in ('icm_gps_test','icm_gps_alarm_test','icm_geocoder_test','icm_gps_historical_test');
-- use information_schema;
-- select DISTINCT CONCAT('update ',table_schema,'.',TABLE_NAME,' set client_permission_id=''icm'';') from columns where column_name='client_permission_id' ;
-- select * from columns where column_name='client_permission_id' ;
-- CONCAT('update ',table_schema,'.',TABLE_NAME,' set client_permission_id=''icm'';')
```

mysqldump --single-transaction --default-character-set=gbk -uabc -pabc -t -w'id=170418406' database_name > id.sql


-t是不增加create table建表和drop table语句
-c是在insert中增加具体的字段名。这样对目的表结构不同原表，情况下更有用

-w后边跟where条件，只导出符合条件的数据

--ssh-keygen -t rsa -b 4096 -C "备注信息"

无外网ip服务器如何访问访问外网?

Linux 代理服务squid 用法
https://www.cnblogs.com/he-ding/p/10038264.html

sysctl list vm.overcommit_memory=1
http://www.redicecn.com/html/Linux/20131125/468.html

ps 命令显示不全
  两种方法

  1.ps-ef |more 哈哈，利用more换行，慢慢看吧，能完全显示了吧

  2.什么？不想翻屏，好吧好吧，仔细看ps的man吧，你会看到这样一行

-w              Wide output. Use this option twice for unlimited width.很简单对吧，看完你就知道怎么用了。是的，是的，知道你很聪明，没错，就是这样滴

ps -efww  OK，完全搞定，所有内容全部显示。

  自此，得出一个结论，man的力量是无穷大滴，大到让你无法想象哦。

  有机会，就来man一下吧！