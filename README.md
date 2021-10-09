# dependencies

Pythonライブラリの依存関係確認用。  
よく使うライブラリのコンフリクトが起きないかチェックする用。

現状だと、`aws-sam-cli` (が依存する`boto3`) が依存する `requests`がコンフリクトしていて最新版(2.26.0)にあげられない。

```sh
> poetry install

SolverProblemError

  Because no versions of aws-sam-cli match >1.33.0,<2.0.0
   and aws-sam-cli (1.33.0) depends on requests (2.25.1), aws-sam-cli (>=1.33.0,<2.0.0) requires requests (2.25.1).
  So, because dependencies depends on both requests (2.26.0) and aws-sam-cli (^1.33.0), version solving failed.
```
