# 自己紹介

宮城広隆 / Hirotaka Miyagi  
1996年8月28日生まれ  

Today I Learned: <https://mh4gf-til.netlify.app/>  
GitHub: <https://github.com/MH4GF>  
Twitter: <https://twitter.com/MH4GF>  
Qiita: <https://qiita.com/mh4gf>  
Zenn: <https://zenn.dev/mh4gf>  
SpeakerDeck: <https://speakerdeck.com/mh4gf>  
ブログ: <https://note.com/mh4gf>  
Instagram: <https://www.instagram.com/mh4gf>

## 経験分野

- Ruby/Rails ... アプリのリリースから、中規模程度になった現在まで2年ほど保守運用 テレビCMによる爆発的なトラフィックを経験
- Go ... CLIツールの作成、echo/gormを使ったAPIサーバーなど
- AWS ... RailsのFargate化/Lambda/API Gateway/SNSなど
- Terraform ... AWSリソースをほぼTerraformで管理
- SaaS ... GCP/Datadog/Sentry/SendGrid/ImageFlux/Hubspotなど
- CI/CD ... Github Actions/Circle CI Testing, Dockerイメージのビルド, ECSへのデプロイなど 

## 得意分野

- スタートアップに求められるリーンでスピードを求められる開発が得意です。
- シード期〜シリーズBの開発チームの変遷や、スクラム開発を経験しています。
- 技術のキャッチアップと現場への適用が得意です。Goの勉強を始めて3ヶ月でCLIツールの作成と本番運用を達成しています。
- Fargateや, DockerでRailsを動かすのが得意です。
- 現在フルリモートで働いており、リモートワークでのコミュニケーションも得意です。

## 興味分野
- 静的型付言語でのバックエンド開発
- モダンWebフロントエンドやサーバレス(Next.js, TS, firebase, lambda)
- IoT
- 0→1, 1→100どちらも
- 人の可能性の後押し、トイルの解消、選択肢を増やす、などの事業
- プログラミングスクールで初学者の方の就職までのお手伝いをしており、エンジニア教育も好きです。

## 経歴

### 2018/6 ~ 現在 Timee, inc.
 
サービスローンチの1ヶ月前にジョイン、初期は1人サーバーサイドとして保守運用を担当  
Railsをメインに、プロダクト/会社の成長とともに幅広い業務を担当させていただきました。

#### 新規事業(PjM/サーバーサイドエンジニア/フロントエンドエンジニア)

新規事業([タイミーデリバリー](https://timee.co.jp/delivery)) のプロジェクトマネジメント・技術選定・設計・実装(Rails, Vue.js)を担当  

- Bizサイドとの折衝、サポートや経理とのオペレーション構築など
- エンジニア3人+デザイナー1人でのプロジェクト進行
- Vue.js/vue-routerを使ったSPAの実装
- 一般的なRailsの環境構築(annotate, rails-erd, bullet, rspec, rubocop)
- 監視/ロギング/CI/CDの導入(Datadog, Sentry, logrageを利用したログのJSON化, CircleCI)
- Railsプロジェクトでの行動指針決め
  - 原則テストコードを書く、書けないなら書けるよう責務を分割する
  - トランザクションやロックなどSQLを正しく適切に書く
  - シンプル・ミニマルに

##### 決済機能の要件定義・技術選定・Stripe APIの実装/運用

- CS/経理/法務とのコミュニケーション、要件定義
- PMFしていないプロダクトでの最小工数になるような技術選定
- Stripe APIを利用した複数サービスを跨ぐ決済トランザクションの実装

[新規事業の決済機能としてStripeを導入する上で考えたこと全て](https://tech.timee.co.jp/entry/2020/12/10/131108)

##### スキーマ駆動開発の導入・運用

- OpenAPI3 + Committeeを利用したスキーマ駆動開発の導入・運用
- ドキュメントの信頼性と保守性を高めた運用が可能に

[Rails + RSpec + OpenAPI3 + Committeeでスキーマ駆動開発を運用するTips](https://tech.timee.co.jp/entry/2020/07/05/150312)  

#### SRE

##### 2020/4 RedashをFargate, Datadog, Terraformで構築/運用

- RedashをFargateでオートスケールできるように
- Datadogによる監視
- それら全てをTerraformで管理

[RedashをFargate, Datadog, Terraformで構築/運用](https://tech.timee.co.jp/entry/2020/04/20/175821)
  
##### 2020/3 ECRのライフサイクルツールの作成

ECSタスクでECRイメージが使われている場合はそのイメージを削除しないようにライフサイクルポリシーを拡張したツールを作成。  
Fargate Scheduled Taskで運用    
<https://github.com/MH4GF/ecr-lifecycle>  
  
##### 2020/3 RailsをFargateでデプロイするチュートリアルの作成

rails new -> generate scaffold -> docker build -> Fargateへのデプロイまでを、  
TerraformでAWSリソースを作って30分程度でデプロイできるようなチュートリアルを作成。  
  
##### 2020/3 RailsアプリをEC2->Fargateに移行  

全社的に移行を進めていたFargate対応の一部を担当。  

- タスク定義を更新するローリングデプロイ
- ALBのリスナールールのpriorityを変更することによるメンテナンス画面表示
- それらを全てchatopsだけで完結できるように

##### 2020/2~ Go製のマイクロサービスの保守、機能追加

echo/gormを利用したマイクロサービスの保守運用を担当 

#### サーバーサイドエンジニア

- 0→1後のサービスの保守運用・負債解消
  - RSpec, Rubocop, OpenAPI3の導入
  - Ruby/Railsのバージョンアップ業
  - APIのバージョニング、Serializerのスキーマ分割
  - index追加
- サービス固有の強いドメインを持つ機能の設計、実装
  - 企業がワーカーをお気に入りリストに追加し、リストにのみバイト案件を限定公開できる機能
  - QRコードを用いたアプリだけで完結するバイト出退勤機能 → [特許を取得しました](https://prtimes.jp/main/html/rd/p/000000057.000036375.html)
  - 契約内容の変更や勤怠管理の機能

##### Railsでリードレプリカへの接続機能

CM放映の負荷分散対応の一つとして、Rails6のマルチDB機能を利用しリードレプリカへの接続機能を実装し本番運用した。  
現在は負荷が下がっているためprimaryだけを見るように設定しており、環境変数を変えるだけでいつでもリードレプリカに接続できるようにしている    
<https://speakerdeck.com/mh4gf/productionderails6marutidbdui-ying-woxiao-sakushi-meru>

## 学歴

- 東京都立小平南高校卒
- 武蔵大学社会学部中退
