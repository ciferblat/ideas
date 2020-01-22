### Несколько deplayment keys на одном компьютере (для разных репозиториев)

Необходимо зайти в папку с репозиторием.
Далее в ней прописать путь к закрытому ключу:

```code
 git config --local core.sshCommand "ssh -i ~/.ssh/id_rsa"
```

### Выпуск сертификата LetsEncrypt

https://github.com/Neilpang/acme.sh

```code
sudo su
apt-get install socat
curl https://get.acme.sh | sh
```

закрываем терминал и открываем заново

```code
sudo su
acme.sh --issue -d mysite.ru -d www.mysite.ru -d api.mysite.ru --standalone
```
