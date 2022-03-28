# cci-aws-hippo



CircleCI を使い、Arm64 環境での(テスト、および) Docker コンテナイメージのビルドと、Amazon ECR 上にイメージの保存を行います。

以下の環境変数をプロジェクトに対して設定しています。

|Name|Value|説明|
|----|-----|----|
|AWS_ACCESS_KEY_ID|(公開しない)|用意したIAMユーザーのアクセスキー|
|AWS_SECRET_ACCESS_KEY|(公開しない)|上記IAMユーザーのシークレットアクセスキー|
|AWS_DEFAULT_REGION|ap-northeast-1|実行リージョン|
|AWS_REGION|ap-northeast-1|実行リージョン|
|AWS_ECR_ACCOUNT_URL|NNNNNNNNNNNN.dkr.ecr.ap-northeast-1.amazonaws.com|Amazon ECR プレイべーとレジストリのURL(NNNNNNNNNNNNはAWSアカウントID)|
|AWS_RESOURCE_NAME_PREFIX|baby-hippo-gram|Amazonリソース名(ARN)のプリフィックス(タグが後続する)|
