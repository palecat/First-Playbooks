## docker.yml

_Playbook_, который будет устанавливать и запускать _Docker_ на локальной машине.

```
ansible-playbook docker.yml -K
```

## mysql.yml

_Playbook_, который будет запускать _MySQL_-сервер на локальной машине. 

```
ansible-playbook mysql.yml -K
```

## user.yml

_Playbook_, который будет на удаленной системе создавать пользователя user1 и задавать ему SSH-ключ (создавая заданный ключ в /home/user1/.ssh/id_rsa.pub). Для шифрования ключа используется ansible-vault. 

```
ansible-playbook user.yml -K --ask-vault-pass
```

## postfix.yml

_Playbook_, который устанавливает, либо удаляет почтовый сервер postfix в зависимости от тега.

```
# установить postfix и запустить с конфигурацией по умолчанию
ansible-playbook postfix.yml -K --tags init
```

```
# удалить postfix
ansible-playbook postfix.yml -K --tags init
```