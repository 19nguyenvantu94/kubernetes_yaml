kubectl apply -f https://raw.githubusercontent.com/RedisLabs/redis-enterprise-k8s-docs/7.4.6-2/bundle.yaml

kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.11.2/deploy/static/provider/cloud/deploy.yaml

kubectl get svc ingress-nginx --namespace=ingress-nginx

kubectl get pods --namespace=ingress-nginx

kubectl get secret rec -o jsonpath='{.data.username}' | base64 --decode

[Text.Encoding]::Utf8.GetString([Convert]::FromBase64String('cmVkaXNkYiwgcmVkaXNkYi1oZWFkbGVzcw=='))

demo@redis.com
NHVNWzii

JbYvrdRV
10402
redisdb, redisdb-headless

kubectl get secret <cluster-name> -o jsonpath='{.data.username}' | base64 --decode
kubectl get secret <cluster-name> -o jsonpath='{.data.password}' | base64 --decode


--- install rabbitmq
kubectl apply -k rabbitmq/.

kubectl create -f https://download.elastic.co/downloads/eck/2.14.0/crds.yaml

kubectl apply -f https://download.elastic.co/downloads/eck/2.14.0/operator.yaml

kubectl -n elastic-system logs -f statefulset.apps/elastic-operator

kubectl create ns sslcert

kubectl create secret tls my-tls-secret --cert=certificate.crt --key=private.key -n sslcert 
kubectl port-forward svc/redis-service 6379:6379  -n redis
kubectl port-forward svc/rabbitmq 15672:15672  -n rabbitmq

helm install rabbitmq bitnami/rabbitmq --namespace rabbitmq --set auth.username=admin --set auth.password=admin123 --set auth.erlangCookie=myCookie --set auth.existingSecret=rabbitmq-secret --set resources.limits.memory="128Mi" --set resources.requests.cpu="0.09" --set resources.requests.memory="128Mi" --set plugins="rabbitmq_management rabbitmq_prometheus rabbitmq_stream"  --set extraConfiguration="log.console.level = info"

helm uninstall rabbitmq --namespace rabbitmq


kubectl get secret rabbitmq-secret -n rabbitmq -o jsonpath="{.data.username}" | base64 -d