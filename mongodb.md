kubectl apply -f https://raw.githubusercontent.com/mongodb/mongodb-enterprise-kubernetes/4.0.14-ent/crds.yaml

kubectl apply -f https://raw.githubusercontent.com/mongodb/mongodb-enterprise-kubernetes/1.30/crds.yaml



kubectl describe deployments mongodb-enterprise-operator -n mongodb

