## FashionablyLate

環境構築

Dockerビルド

1. `git clone git@github.com:estra-inc/confirmation-test-contact-form.git`
2. docker compose up -d --build

>Silicon製CPUのMacの場合は「no matching manifest for linux/arm64/v8 in the manifest list entries」とエラーメッセージが出てビルド出来ない場合があります。その場合はdocker-compose.ymlファイルの「mysql」と「phpmyadmin」内の「image」の項目を修正してください

```
mysql:
    image: mysql:8.0(この文を修正)
    environment:
```
```
phpmyadmin:
    image: phpmyadmin:latest(この文を修正)
    environment:
```

3. DockerDesktopアプリを立ち上げる
