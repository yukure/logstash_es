# Elasticsearch + Kibana + LogStash

- docker-composeで環境を構築
  - Elastcsearch (7.2) - single nodeで起動
  - Logstash (6.8.3) jdkの関係で、こっちのバージョン使用している
- Docker Desktop のメモリ割り当てを３GBぐらいにしておくと良いかも
  - `docker-compose up` をした際に、`elasticsearch`のコンテナが1GBぐらいメモリを食ってしまう。これにより、他のコンテナがすでに起動していた場合に、`elasticsearch`のコンテナが起動途中で終了してしまう可能性があるため。