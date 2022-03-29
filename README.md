# cci-aws-hippo



AWS CloudFormation を使い、AWS Graviton 環境での AWS Fargate 実行環境を定義し、CircleCI を使って実環境を構築しています。

その後、子カバアプリのコンテナイメージを Amazon ECR に登録し(前述)、そのコンテナイメージを使って、Fargate のタスクを更新します。

なお、以下の環境変数をプロジェクトに対して設定しています(前ステップと同じ)。

|Name|Value|説明|
|----|-----|----|
|AWS_ACCESS_KEY_ID|(公開しない)|用意したIAMユーザーのアクセスキー|
|AWS_SECRET_ACCESS_KEY|(公開しない)|上記IAMユーザーのシークレットアクセスキー|
|AWS_DEFAULT_REGION|ap-northeast-1|実行リージョン|
|AWS_REGION|ap-northeast-1|実行リージョン|
|AWS_ECR_ACCOUNT_URL|NNNNNNNNNNNN.dkr.ecr.ap-northeast-1.amazonaws.com|Amazon ECR プレイべーとレジストリのURL(NNNNNNNNNNNNはAWSアカウントID)|
|AWS_RESOURCE_NAME_PREFIX|baby-hippo-gram|Amazonリソース名(ARN)のプリフィックス(タグが後続する)|
