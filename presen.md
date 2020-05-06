---
marp: true
class: invert
page: number
paginate: true
---

## ポータルサイトとSysAd係
### 53代 Tsuzu

@MIS.Works Exhibition 2020

---
![bg contain right:33%](./icon.jpg)

# だれ?
- 53代 Tsuzu
- 基幹理工学部情報理工学科3年
- SysAd係・Web班長
- 好きなもの: Go言語、Kubernetes、Gopherくん(?)
- Twitter: [@Wp120_3238](https://twitter.com/Wp120_3238)、[@tsuzu_misw](https://twitter.com/tsuzu_misw)(みす垢)
- GitHub: [cs3238-tsuzu](https://github.com/cs3238-tsuzu)

---
# Agenda
- SysAd係とは?
- ポータルサイト
    - ポータルサイトって何?
    - デモ
    - 仕組み(技術的な)
- 終わりに

---
# SysAd係とは?
- サークル内のシステム諸々を管理する係
- 去年の3月から新設(元々はWeb班長or幹事長の仕事)
- サービス等: Kibela、Slack?
- 契約: misw.jpドメイン、レンタルサーバ
- その他: 部室のサーバ、ルータ、ネットワーク回線、info@misw.jp
- メンバー: @Tsuzu, @tosuke

---
# 宣伝
- ブログ記事
    - [MIS.Wを支えるSysAd係の今までとこれから【カウントダウンカレンダー2019冬 5日目】](https://blog.misw.jp/entry/2019/12/16/000000)
    - [ブラウザでWebページが開かれるまで【新歓ブログリレー2020 14日目】](https://blog.misw.jp/entry/2020/04/14/000000)
---

# ポータルサイト

---

# ポータルサイトとは?
- サークルに所属してるメンバーを一括で管理できるサービス
- https://portal.misw.jp/
- モチベーション
    - 毎度別のGoogle Formsで散乱しがちな情報の一極化
    - Slackのメンバー管理をきちんとした方

---

# ポータルサイトとは
- 機能
    - サークルへの入会手続き
    - 会費は支払済かどうか
    - Slackへの半自動招待
    - 会員情報の登録
    - QRコードをベースとした支払い確認(予定変更で未実装)
    - などなど

---

# デモ

---

# 仕組み
- フロントエンド: TypeScript + React + Next.js + Material-UI
- バックエンド: Go + echo v4
- インフラ: Kubernetes(MISW Servers)

---
![bg contain right:33%](./auth0-logo-fordarkbg.png)

# Login with Slack via Auth0
- Slackでログイン
- 招待後のSlackIDはWebhookでポータルに自動登録

---

![bg contain right:60%](./スクリーンショット%202020-05-06%2013.34.12.png)

# mischan-bot
- GitOpsのためのBOT
- Goで実装
- GitHub App(Bot)

---
# おわりに
MISWとWeb班、そしてSysAd係へぜひ！