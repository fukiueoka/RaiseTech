# AWSコース第4回講義　課題  

## VPC
- リソースマップ
![VPCリソースマップ](/images/lecture.04/raisetechvpc.png)

## EC2
- 概要
![EC2概要](/images/lecture.04/test-webserver.png)
- セキュリティグループ
![EC2セキュリティグループ](/images/lecture.04/t-webserver_sec.png)

## RDS
- 概要
![RDS概要](/images/lecture.04/datebase-1.png)
- セキュリティグループ（インバウンドルール）
![RDSセキュリティ（in）](/images/lecture.04/datebase-1_sec_in.png)
- セキュリティグループ（アウトバウンドルール）
![RDSセキュリティ（out）](/images/lecture.04/datebase-1_sec_out.png)

## EC2からRDSへの接続を確認（MySQL）
![EC2からRDSへアクセス](/images/lecture.04/ec2-rds_conenction.png)

## 感想
- AWSを使用してインフラ構築していく上で重要な単語が多く出たため、そのインプットに時間がかかった。
- VPC作成にあたっては、それぞれのサブネットやゲートウェイ、セキュリティグループ含め、  
  関係性と量的なイメージを図などを用いて整理し、明示できることが重要だと実感できた。