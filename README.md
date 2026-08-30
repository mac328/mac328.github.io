# mac328.github.io

`https://mac328.github.io/` （ドメインの一番上）を配信するためだけのリポジトリ。

## なぜ必要か

AdMob の **app-ads.txt** は、Play ストアに登録した「デベロッパー ウェブサイト」の
**ドメインの一番上**に置かないと読まれない。

- 読まれる: `https://mac328.github.io/app-ads.txt` ← このリポジトリ
- 読まれない: `https://mac328.github.io/eiken-dojo/app-ads.txt`

アプリ本体（英検準2級 反復トレ）は別リポジトリ `mac328/eiken-dojo` にあり、
`https://mac328.github.io/eiken-dojo/` で公開している。**そちらは触らない。**

## app-ads.txt の中身

```
google.com, pub-4259051521565413, DIRECT, f08c47fec0942fa0
```

`pub-4259051521565413` は AdMob のパブリッシャー ID。
広告ユニット ID ではないので取り違えないこと。
中身は AdMob の「アプリの設定 → アプリの確認」に表示される行をそのまま使う。

## 直したあとにやること

1. `https://mac328.github.io/app-ads.txt` がブラウザで開けるか確かめる
2. AdMob → アプリ → 英検準2級 反復トレ → アプリの設定 → **Verify app**
3. 「アプリの確認」が **確認済み** になれば成功（クローラが来るまで最大24時間）

## 注意

- ファイル名は `app-ads.txt`。`ads.txt`（ウェブサイト用）とは別物
- フォルダに入れず、リポジトリの直下に置くこと
- Play ストアの掲載情報に「ウェブサイト」が登録されていないと、
  そもそも確認が始まらない
