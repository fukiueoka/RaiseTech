# 第6回課題
## 概要　　　
 1. テンプレートファイル, スタック作成を確認   
 2. 各リソースの構築を確認   
  a. VPC   
  b. EC2   
  c. RDS   
  d. S3   
  e. IAMRole   
  f. ALB   
 3. リソース間の接続確認   
  a. EC2にMyPCよりSSH接続    
  b. EC2からRDSに接続   
  c. EC2からS3へファイルのアップロード   

## 1. テンプレートファイル, スタック生成を確認
 - [**lecture10_vpc.yml**](/lec10_cftemplate/lecture10_vpc.yml)
 - [**lecture10_security.yml**](/lec10_cftemplate/lecture10_security.yml)
 - [**lecture10_resources.yml**](/lec10_cftemplate/lecture10_resources.yml)   
 - 作成したスタック   
 ![スタック作成](/images/lecture.10/stack_cfn.png)  
 
## 2. 各リソースの構築を確認
 a. VPC 構築結果   
 ![vpcをCFnにより構築](/images/lecture.10/vpc-cfn.png)   
 b. EC2 構築結果   
 ![ec2をCFnにより構築](/images/lecture.10/ec2-cfn.png)   　　  
 c. RDS 構築結果    
 ![rdsをCFnにより構築](/images/lecture.10/rds-cfn.png)   
 d. S3 構築結果   
 ![s3をCFnにより構築](/images/lecture.10/s3bucket-cfn.png)     
 f. IAMRole 構築結果      
 ![iamroleをCFnにより構築](/images/lecture.10/iamrole-cfn.png)    
 f. ALB 構築結果   
 ![albをCFnにより構築](/images/lecture.10/alb-cfn.png)   

## 3. リソース間の接続確認 　　
 a&b. EC2にMyPCよりSSH接続および、EC2からRDSに接続   
 ![EC2からRDSへ接続&EC2からS3へアップロード](/images/lecture.10/ec2(ssh)_ec2-rds_connection.png)    
 c. EC2からS3へファイルをアップロード（EC2に付与したS3に関する権限を確認）   
 ![EC2からS3へテキストアップロード](/images/lecture.10/ec2-s3_connection.png)   
 