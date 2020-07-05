## Домашнее задание  
LDAP  
Цель: В результате выполнения ДЗ студент установит FreeIPA.  
1. Установить FreeIPA;  
2. Написать Ansible playbook для конфигурации клиента;  
3*. Настроить аутентификацию по SSH-ключам;  
4**. Firewall должен быть включен на сервере и на клиенте.  

## Решение    
Депллой стенда производится из каталога `./homework`  
```
git clone
cd ./26.LDAP/homework
vagrant up
```
Аккаунт создаваемый после деплоя, при выполнения входа потребуется сменить пароль   
```
login:    user
password: 12345678
```
Для подключения к графическому управления на хосте с которого осуществляется вход, необходимо добавить запись в `/etc/hosts`  

```
cat<<EOF>>/etc/hosts
192.168.100.101 ipa-server.dmosk.local
EOF
```

работает подключение по `ssh`, также включен `firewalld`  
Учетная запись администратора  `LDAP`  
```
login: admin
password: 12345678
```
