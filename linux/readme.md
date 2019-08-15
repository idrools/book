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


