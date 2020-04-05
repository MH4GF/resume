# 自己紹介

宮城広隆 / Hirotaka Miyagi  
1996年8月28日生まれ  
  
GitHub: <https://github.com/MH4GF>  
Twitter: <https://twitter.com/MH4GF>  
Qiita: <https://qiita.com/mh4gf>  
SpeakerDeck: <https://speakerdeck.com/mh4gf>  
ブログ: <https://note.com/mh4gf>  
Instagram: <https://www.instagram.com/mh4gf>

## 経験分野

- Ruby/Rails ... アプリのリリースから、中規模程度になるまで2年ほど保守運用 テレビCMによる爆発的なトラフィックを経験
- Go ... CLIツールの作成、echo/gormを使ったWebアプリケーションなど
- AWS ... RailsのFargate化/Lambda/API Gateway/SNSなど
- Terraform ... AWSリソースをほぼTerraformで管理
- SaaS ... Datadog/Sentry/SendGridなど

# 経歴

## Timee, inc. 

2018/7/5 ~ 現在  

### 2020/3 ECRのライフサイクルツールの作成

ECSタスクでECRイメージが使われている場合はそのイメージを削除しないようにライフサイクルポリシーを拡張したツールを作成。  
Fargate Scheduled Taskで運用    
<https://github.com/MH4GF/ecr-lifecycle>  
  
### 2020/3 RailsをFargateでデプロイするチュートリアルの作成

rails new -> generate scaffold -> docker build -> Fargateへのデプロイまでを、  
TerraformでAWSリソースを作って30分程度でデプロイできるようなチュートリアルを作成。  
  
### 2020/3 RailsアプリをEC2->Fargateに移行  

全社的に移行を進めていたFargate対応の一部を担当。  

- タスク定義を更新するローリングデプロイ
- ALBのリスナールールのpriorityを変更することによるメンテナンス画面表示
- それらを全てchatopsだけで完結できるように

### 2020/2~ Go製のマイクロサービスの保守、機能追加

echo/gormを利用したマイクロサービスの保守運用を担当 

### 2020/1 FirebaseDynamicLinkを利用したディープリンク機能

サーバーサイドでFDL APIを叩いてアプリのシェア用URLを生成するライブラリを作成    

### 2019/12 RailsアプリケーションをマルチDBに対応

CM対応の負荷分散対応の一つとして、Rails6のマルチDB対応を利用しリードレプリカに接続できるようにして本番運用した。  
現在は負荷が下がっているためprimaryだけを見るように設定しており、環境変数を変えるだけでいつでもリードレプリカに接続できるようにしている    
<https://speakerdeck.com/mh4gf/productionderails6marutidbdui-ying-woxiao-sakushi-meru>

### 2019/9 Rails6.0.1.2へのバージョンアップ
  
バージョンアップに備えて事前にDependabotを導入し、依存しているGemのバージョンアップを着実に進めた後Railsのバージョンアップを実行  
Rails6リリースから1ヶ月以内に本番運用することができた  
  
### 2019/8 SwaggerUIのホスティングと自動デプロイ

AWS Amplifyを利用してSwaggerUIをPRのマージでデプロイできるようにした
<https://qiita.com/mh4gf/items/1ae98ccb946b71de61ec>

### プッシュ通知機能の実装 
- 2019/7 FCMを利用したAndroid端末向けのプッシュ通知機能の実装
- 2018/12 SNSを利用したiOS端末向けプッシュ通知機能の実装 

FCMの方が諸々使い慣れています。  

### サービス固有の強いドメインを持つ機能の設計、実装

- 企業がワーカーをお気に入りリストに追加し、リストにのみバイト案件を限定公開できる機能
- QRコードを用いたアプリだけで完結するバイト出退勤機能
- 契約内容の変更や勤怠管理の機能

### 2018/8~2019/1 タイミーサーバーサイド1人開発期

リリース期の業務委託メンバーは契約が終了し、サーバーサイドメンバーは自分1人、iOSエンジニアが1人、加えてCTOというメンバーで保守運用していくことになりました。  
Webアプリに加えてAPIサーバーの保守も担当。バグが報告されたら解消しつつ、Featureの機能を開発し続けました。CS/セールス/経理業務など他部署のオペレーションも手伝いつつ、相談しながら少しずつ機能として落とし込んでいきました。

### 2018/7~8 ジョイン、タイミー初期開発

2018/7/6にジョイン。  
1ヶ月という短い納期でサービスをリリースするため、Rails + BootStrap + jQueryという構成で最小限の機能でのリリースを目指し、2018/8/10にリリース。  
タイミーは当時ワーカー向けiOSアプリとAPIサーバー、企業向け管理用Webアプリがあり、自身はWebアプリ側を担当。  

## 学歴

- 東京都立小平南高校卒
- 武蔵大学社会学部中退

