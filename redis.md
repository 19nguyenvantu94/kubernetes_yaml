kubectl apply -f https://raw.githubusercontent.com/RedisLabs/redis-enterprise-k8s-docs/7.4.6-2/bundle.yaml

kubectl get secret rec -o jsonpath='{.data.username}' | base64 --decode

[Text.Encoding]::Utf8.GetString([Convert]::FromBase64String('cmVkaXNkYiwgcmVkaXNkYi1oZWFkbGVzcw=='))

demo@redis.com
NHVNWzii

JbYvrdRV
10402
redisdb, redisdb-headless

kubectl get secret <cluster-name> -o jsonpath='{.data.username}' | base64 --decode
kubectl get secret <cluster-name> -o jsonpath='{.data.password}' | base64 --decode