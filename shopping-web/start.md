
#### 虚拟环境   
开启worker,         
列出所有：lsvirtualenv    
workon df-env (退出 deactivate)     

#### requirements.txt用来记录项目所有的依赖包和版本号:     
```pip freeze >requirements.txt```    

安装requirement.txt:    
```pip install -r requirements.txt```  


建立索引数据  
python manage.py rebuild_index

----
### Linux    
#### mysql    
mysql -uroot -p     
password: Mathkk123+-      

查看运行状态     
systemctl status mysqld.service     


#### redis    
检查端口： netstat -ltnp |grep 6379    
启动：  service redisd start      
关闭：  service redisd stop      

可进入终端    
cd /usr/local/redis-5.0-rc3/src    
./redis-cli    
查看库  
select 1
所有数据   
keys * hgetall cart_2    



#### celery启动异步注册任务
#### 虚拟环境   
开启worker,     (退出 deactivate)     
workon df-env    

在项目目录下执行：cd /opt/dailyfresh-celerytasks    
```celery -A celery_tasks.tasks worker -Q queue --loglevel=info```     
或     
```celery -A celery_tasks.tasks worker --loglevel=info ```    


##### FastDFS启动分布式文件存储系统
##### 启动fastdfs服务命令如下：   
```service fdfs_trackerd start```   
```service fdfs_storaged start```   

#### 测试Tracker 和 Storage 服务通信       
/usr/bin/fdfs_monitor /etc/fdfs/storage.conf     

#### 查看服务    
netstat -unltp|grep fdfs     


#### nginx   
#### 启动nginx   
cd /usr/local/nginx/sbin/   
./nginx   

#### 查看nginx服务   
ps aux|grep nginx    








