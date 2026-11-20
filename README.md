# Batting Log Share

野球打率ノートの招待リンク用ブリッジページです。

## URL

```text
https://soku-ma.github.io/batting-log-share/?code=XXXX
https://soku-ma.github.io/batting-log-share/invite.html?code=XXXX
```

## 役割

- SNSやメモアプリでリンク化されやすいHTTPS URLを提供する
- 招待コードを表示する
- アプリが入っているユーザー向けに `battinglog://share-invite?code=...` を開く
- 未インストールユーザー向けにApp Store / Google Playへ誘導する
- ブラウザ言語に応じて日本語/英語の文面と公式ストアバッジを出し分ける

このページではSupabaseへ問い合わせません。招待コードの検証はアプリ内の `accept_invite` RPCで行います。

## ストアのリンクの流入元

「アプリがない場合」のストアのボタンには、インストール数を数えるための印を付けています。

- App Store: `pt=122938945&ct=share_invite_page&mt=8`（App Store Connect の「キャンペーン」で見る）
- Google Play: `referrer` に `utm_source=batting-log&utm_medium=share&utm_campaign=share_invite_page`

アプリが送る招待の文章に直接書くストアのリンクは `share_invite` です（ページ経由と分けて数える）。
