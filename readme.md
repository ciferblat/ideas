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
Результат:

```code
[Wed Jan 22 18:10:07 MSK 2020] Your cert is in  /root/.acme.sh/mysite.ru/auto-doc24.ru.cer 
[Wed Jan 22 18:10:07 MSK 2020] Your cert key is in  /root/.acme.sh/mysite.ru/auto-doc24.ru.key 
[Wed Jan 22 18:10:07 MSK 2020] The intermediate CA cert is in  /root/.acme.sh/mysite.ru/ca.cer 
[Wed Jan 22 18:10:07 MSK 2020] And the full chain certs is there:  /root/.acme.sh/mysite.ru/fullchain.cer 
```
### VS Code: Отладка приложения NestJS, созданного nrwl 

В launch.json добавляем:

```json
{
    "type": "node",
    "request": "launch",
    "name": "Effective Date",
    "program": "${workspaceFolder}/apps/extensions/effective-date/src/main.ts",
    "preLaunchTask": "tsc: watch - apps/extensions/effective-date/tsconfig.build.json",
    "outFiles": ["${workspaceFolder}/dist/**/*.js"],
    "skipFiles": [
        "${workspaceFolder}/node_modules/**/*.js",
        "<node_internals>/**/*.js"
    ]
}
```

В tasks.json:

```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "type": "typescript",
      "tsconfig": "apps/extensions/effective-date/tsconfig.build.json",
      "option": "watch",
      "problemMatcher": ["$tsc-watch"],
      "group": "build",
      "label": "tsc: watch - apps/extensions/effective-date/tsconfig.build.json"
    }
  ]
}
```

### Пример disclaimer'а по услуге

https://dxtra.markets.reuters.com/Dx/DxnHtm/Pub_Docs/legal.htm
