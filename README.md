# test-app-gitops

このリポジトリは 1 回の払い出し専用です。共有の platform-gitops には置きません。

- `config.json` は同期先 Namespace とアプリ名。ApplicationSet が読む。`apiVersion` は無い
- Namespace `test-app`
- Deployment `test-app` replicas 2
- ServiceAccount の `eks.amazonaws.com/role-arn` は `arn:aws:iam::977099000999:role/s3read-test-app-test-app`
- Pipeline が CloudFormation でバケット `test-app-202610` と IAM ロールを作り、イメージをビルドします
