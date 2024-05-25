# 第5回課題
## 1. EC2 上にサンプルアプリケーションをデプロイ
### 組み込みサーバーを使用した動作確認
 - 動作確認
 　![組み込みサーバー](/images/lecture.05/01_existingpuma_startapweb.png)

### Webサーバー(Nginx)とAPサーバー(Puma)に分離して動作確認
 - EC2のセキュリティグループのインバウンドは80番ポート許可
 　![80ポートをインバウンド](/images/lecture.05/02_ec2sec_in_allow80port.png)
 - UnixSocketを使ったPumaの動作確認
 　![puma単体動作確認](/images/lecture.05/02_puma_unixsock_connectap.png)
 - Nginx単体での起動を確認
 　![Nginx単体起動](/images/lecture.05/02_nginx_startup.png)
 - NginxとPumaをUnixSocketを通して連携した上でサンプルAPの動作確認
 　![Nginxpuma連携](/images/lecture.05/02_nginxpuma_connectap.png)

## 2. ELB追加
### ALBの作成
   ![ALB概要](/images/lecture.05/03_alb_setting.png)

### セキュリティグループ
 - ELBのインバウンドは80番許可（EC2のセキュリティグループ構成と同じ）
   ![ELBインバウンド](/images/lecture.05/03_elbsec_in_allow80port.png)
 - EC2のインバウンドはELBからの通信を許可
   ![EC2インバウンド（ALB）](/images/lecture.05/03_ec2sec_in_allowELB.png)

### ALBから接続して動作確認
   ![ALBで起動](/images/lecture.05/03_alb_nginxpuma_apconnect.png)
   
## 3. サンプルAPの画像保存先としてS3を追加
### EC2にアクセス権限があるS3バケットを作成
 - S3バケット作成
   ![s3バケット概要](/images/lecture.05/04_s3backet_cre.png)
 - アクセス権限をEC2に付与（S3へのアクセス権限を許可するIAMロールをEC2にアタッチ）
   ![IAMロールアタッチ](/images/lecture.05/04_s3role_attach_ec2.png)

### S3に画像を保存
 - サンプルAPに画像を保存
   ![APに画像保存](/images/lecture.05/04_imagesave_onbrowserap.png)
 - S3に上記画像が保存されていることを確認
   ![S3に画像保存](/images/lecture.05/04_s3bucket_download.png)

## 4.aws構成図  
   ![aws環境構成図](/images/lecture.05/05_lesson05sad.drawio.png)