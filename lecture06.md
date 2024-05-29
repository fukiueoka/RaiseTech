# 第6回課題
## 1. CloudTrailにてログを確認する （選んだイベントに関して、内容を3つ取り上げる）
 ・"eventTime": "2024-05-24T08:30:40Z"  
 ・"eventSource": "ssm.amazonaws.com"  
 ・"eventName": "GetConnectionStatus"  
 ![イベント名](/images/lecture.06/cloudtrail-exevent.png)
 ![イベント詳細](/images/lecture.06/cloudtrail-eventrecord.png)
 
## 2. CloudWatchアラームを設定する（ALBのアラームの設定、メール通知）
 ・Railsアプリが使えない状態（Rails停止時）   
 ![アラーム詳細](/images/lecture.06/cloudwatch-alarm.png)
 ![アラームメール](/images/lecture.06/cloudwatch-alarm-email.png)  
 ・Railsアプリが使える状態（Rails起動時）  
 ![OK詳細](/images/lecture.06/cloudwatch-ok.png)
 ![OKメール](/images/lecture.06/cloudwatch-ok-email.png)

## 3. AWS利用料の見積を作成する 
 ・使用ツール：AWS Pricing Calculator  
 ・〔共有URL〕https://calculator.aws/#/estimate?id=77ee0c728893d65195049159fa68da96c8905239
 
## 4. 現在の利用料金を確認する
 ・EC2の利用料金は無料利用枠内（free tier）で収まっていた。   
 ・VPCに関して課金が発生していた。これは”IPv4アドレスの使用”によるもので、1ヶ月750時間の無料枠を超過したためだと考えられる。   
 　→ IPv4アドレスの使用に関しても管理が必要だと感じた。   
![請求額](/images/lecture.06/billing-total.png)
![請求詳細](/images/lecture.06/billing-detail.png)