## FashionablyLate

環境構築

Docker構築

1. `git clone git@github.com:estra-inc/confirmation-test-contact-form.git`
2. docker compose up -d --build

>Silicon製CPUのMacの場合は「no matching manifest for linux/arm64/v8 in the manifest list entries」とエラーメッセージが出てビルド出来ない場合があります。その場合はdocker-compose.ymlファイルの「mysql」内に「platform」の項目を追加で記載してください

```
mysql:
    platform: linux/x86_64(この文追加)
    image: mysql:8.0.26
    environment:
```
