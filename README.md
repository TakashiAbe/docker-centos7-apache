## 概要

### Apache2.4 on CentOS7

- Systemd導入
- Crond導入
- 日本語化
- タイムゾーンを東京へ変更
- gitインストール
- Apache2.4

## 使い方

```
docker run -d --privileged=true --name centos7-apache -p 80:80 -v /var/docker-volume:/var/www/html:rw takashiabe/centos7-apache
```

docker-compose で使う際も、privileged: true の指定を忘れずに入れてください。
document_root は /var/www/html です。

systemdが動きますので、Apacheの（リロード|リスタート）は

```
docker exec -it centos7-apache systemctl (reload|restart) httpd.service
```

です。


## License
MIT