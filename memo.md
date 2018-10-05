[今更ながらRails5+line-bot-sdk-ruby+HerokuでLineBot作成してみたら、色々詰まったのでまとめました。 - Qiita](https://qiita.com/y428_b/items/d2b1a376f5900aea30dc)の手順に沿って
rails server の後ローカルに接続できず。

[PostgresSQL のerror　Postgres PG::ConnectionBad: could not connect to server: No such file or directory Is the server running locally and accepting connections on Unix domain socket "/tmp/.s.PGSQL.5432"? - Qiita](https://qiita.com/yoshixj/items/3d742eb08343ea93dcd4)
こういう状況になったので
```bash
$ brew services start postgresql
$ brew services stop postgresql
$ brew services restart postgresql
```

その後、
FATAL: database "tanita_development" does not exist
といわれたのでとりあえず
`$ createdb tanita_development`したら起動できた。