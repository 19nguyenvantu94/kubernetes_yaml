kubectl apply -f https://raw.githubusercontent.com/RedisLabs/redis-enterprise-k8s-docs/7.4.6-2/bundle.yaml

kubectl get secret rec -o jsonpath='{.data.username}' | base64 --decode

[Text.Encoding]::Utf8.GetString([Convert]::FromBase64String('TkhWTld6aWk='))

demo@redis.com
NHVNWzii