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
- CI/CD ... Dockerイメージのビルド、ECSへのデプロイなど Github Actions/Circle CI

## 得意分野

- スタートアップに求められるリーンでスピードを求められる開発が得意です。
- シード期〜シリーズBの開発チームの変遷や、スクラム開発を経験しています。
- 技術のキャッチアップと現場への適用が得意です。Goの勉強を始めて3ヶ月でCLIツールの作成と本番運用を達成しています。
- Fargateや, dockerでRailsを動かすのが得意です。
- 現在フルリモートで働いており、リモートワークでのコミュニケーションも得意です。
- プログラミングスクールで初学者の方の就職までのお手伝いをしており、エンジニア教育も好きです。

## 経歴

### 2018/6 ~ 現在 Timee, inc.
 
サービスローンチの1ヶ月前にジョイン、初期は1人サーバーサイドとして保守運用を担当  
Railsをメインに、プロダクトの成長とともに幅広い業務を担当させていただきました。

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
