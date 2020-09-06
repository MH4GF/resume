# 自己紹介

宮城広隆 / Hirotaka Miyagi  
1996年8月28日生まれ  

Today I Learned: <https://mh4gf-til.netlify.app/>
GitHub: <https://github.com/MH4GF>  
Twitter: <https://twitter.com/MH4GF>  
Qiita: <https://qiita.com/mh4gf>  
SpeakerDeck: <https://speakerdeck.com/mh4gf>  
ブログ: <https://note.com/mh4gf>  
Instagram: <https://www.instagram.com/mh4gf>

## 経験分野

- Ruby/Rails ... アプリのリリースから、中規模程度になった現在まで2年ほど保守運用 テレビCMによる爆発的なトラフィックを経験
- Go ... CLIツールの作成、echo/gormを使ったAPIサーバーなど
- AWS ... RailsのFargate化/Lambda/API Gateway/SNSなど
- Terraform ... AWSリソースをほぼTerraformで管理
- SaaS ... GCP/Datadog/Sentry/SendGrid/ImageFlux/CircleCIなど

## 得意分野

- スタートアップに求められるリーンでスピードを求められる開発が得意です。
- シード期〜シリーズBの開発チームの変遷や、スクラム開発を経験しています。
- 技術のキャッチアップと現場への適用が得意です。Goの勉強を始めて3ヶ月でCLIツールの作成と本番運用を達成しています。
- Fargateや, dockerでRailsを動かすのが得意です。
- 現在フルリモートで働いており、リモートワークでのコミュニケーションも得意です。
- プログラミングスクールで初学者の方の就職までのお手伝いをしており、エンジニア教育も好きです。

## 経歴

### Timee, inc. (SRE)

2020/2/1 ~ 現在  
サーバーサイドエンジニアからSREにポジションを変えました。新機能の開発はメンバーに託し、今後もスケールしていくサービスを見据えた基盤設計と運用に注力しています。  

#### 2020/4 RedashをFargate, Datadog, Terraformで構築/運用

- RedashをFargateでオートスケールできるように
- Datadogによる監視
- それら全てをTerraformで管理

[RedashをFargate, Datadog, Terraformで構築/運用](https://tech.timee.co.jp/entry/2020/04/20/175821)
  
#### 2020/3 ECRのライフサイクルツールの作成

ECSタスクでECRイメージが使われている場合はそのイメージを削除しないようにライフサイクルポリシーを拡張したツールを作成。  
Fargate Scheduled Taskで運用    
<https://github.com/MH4GF/ecr-lifecycle>  
  
#### 2020/3 RailsをFargateでデプロイするチュートリアルの作成

rails new -> generate scaffold -> docker build -> Fargateへのデプロイまでを、  
TerraformでAWSリソースを作って30分程度でデプロイできるようなチュートリアルを作成。  
  
#### 2020/3 RailsアプリをEC2->Fargateに移行  

全社的に移行を進めていたFargate対応の一部を担当。  

- タスク定義を更新するローリングデプロイ
- ALBのリスナールールのpriorityを変更することによるメンテナンス画面表示
- それらを全てchatopsだけで完結できるように

#### 2020/2~ Go製のマイクロサービスの保守、機能追加

echo/gormを利用したマイクロサービスの保守運用を担当 
  
.  
.  
.  

### Timee, inc. (サーバーサイドエンジニア)

2018/7/6 ~ 2020/1/31  
タイミーアプリのリリース前からジョインし、ネイティブアプリ向けAPIサーバー, 企業向けWebアプリの保守運用,新規開発を全般的に担当しました。

#### 2020/1 FirebaseDynamicLinkを利用したディープリンク機能

サーバーサイドでFDL APIを叩いてアプリのシェア用URLを生成する機能を実装    

#### 2019/12 Railsでリードレプリカへの接続機能

CM放映の負荷分散対応の一つとして、Rails6のマルチDB機能を利用しリードレプリカへの接続機能を実装し本番運用した。  
現在は負荷が下がっているためprimaryだけを見るように設定しており、環境変数を変えるだけでいつでもリードレプリカに接続できるようにしている    
<https://speakerdeck.com/mh4gf/productionderails6marutidbdui-ying-woxiao-sakushi-meru>

#### 2019/9 Rails6へのアップデート
  
事前にDependabotを導入し、依存しているGemのアップデートを着実に進めた後Railsのアップデートを実行  
Rails6のリリースから1ヶ月以内に本番運用することができた  
  
#### 2019/8 SwaggerUIのホスティングと自動デプロイ

AWS Amplifyを利用してSwaggerUIをPRのマージでデプロイできるように。
<https://qiita.com/mh4gf/items/1ae98ccb946b71de61ec>

#### サービス固有の強いドメインを持つ機能の設計、実装

- 企業がワーカーをお気に入りリストに追加し、リストにのみバイト案件を限定公開できる機能
- QRコードを用いたアプリだけで完結するバイト出退勤機能 -> [特許を取得しました](https://prtimes.jp/main/html/rd/p/000000057.000036375.html)
- 契約内容の変更や勤怠管理の機能

#### プッシュ通知機能の実装 
- 2019/7 FCMを利用したAndroid端末向けのプッシュ通知機能の実装
- 2018/12 SNSを利用したiOS端末向けプッシュ通知機能の実装 

FCMの方が諸々使い慣れています。  

#### 2018/8~2019/1 タイミーサーバーサイド1人開発期

リリース期の業務委託メンバーは契約が終了し、サーバーサイドメンバーは自分1人、iOSエンジニアが1人、加えてCTOというメンバーで保守運用していくことになりました。  
Webアプリに加えてAPIサーバーの保守も担当。バグが報告されたら解消しつつ、Featureの機能を開発し続けました。CS/セールス/経理業務など他部署のオペレーションも手伝いつつ、相談しながら少しずつ機能として落とし込んでいきました。

#### 2018/7~8 ジョイン、タイミー初期開発

2018/7/6にジョイン。当時はRailsチュートリアルが終わった程度の業務未経験でした。  
1ヶ月という短い納期でサービスをリリースするため、Rails + BootStrap + jQueryという構成で最小限の機能でのリリースを目指し、2018/8/10にリリース。  
タイミーは当時ワーカー向けiOSアプリとAPIサーバー、企業向け管理用Webアプリがあり、自身はWebアプリ側を担当。  

## 学歴

- 東京都立小平南高校卒
- 武蔵大学社会学部中退

