##rabbitmq


* 설치

```
sudo scp choihyunjee@172.27.66.159:/Users/choihyunjee/Downloads/erlang-19.0.4-1.el6.x86_64.rpm /daum/install/
sudo scp choihyunjee@172.27.66.159:/Users/choihyunjee/Downloads/rabbitmq-server-3.6.12-1.el7.noarch.rpm /daum/install/
sudo rpm -Uvh /daum/install/erlang-19.0.4-1.el6.x86_64.rpm
sudo rpm -Uvh /daum/install/rabbitmq-server-3.6.12-1.el7.noarch.rpm
sudo yum install socat
sudo rpm -Uvh /daum/install/rabbitmq-server-3.6.12-1.el7.noarch.rpm
```

* 실행

```
sudo rabbitmq-server -detached
```

* management 설치 - 화면으로 보기 위한
```
sudo rabbitmq-plugins enable rabbitmq_management
ps -ef | grep rabbit
```

* 사용자/권한 추가 
````
sudo rabbitmqctl add_user username password
sudo rabbitmqctl set_user_tags username administrator
sudo rabbitmqctl set_permissions username ".*" ".*" ".*"
````

* 클러스터링
 ** var/lib/rabbitmq/.erlang.cookie 복사해서 같은 위치로 클러스터링할 서버들에 붙여넣음
 
```
sudo rabbitmqctl stop
sudo scp choihyunjee@172.27.66.159:/Users/choihyunjee/.erlang.cookie.egis-rabbitmq-test01 /var/lib/rabbitmq/.erlang.cookie
sudo rabbitmq-server -detached
sudo rabbitmqctl stop_app
sudo rabbitmqctl join_cluster rabbit@서버_네임
sudo rabbitmqctl start_app
sudo rabbitmqctl cluster_status
```
