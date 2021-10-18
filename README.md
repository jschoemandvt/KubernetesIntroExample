### Repository for the K8s in 1 hour video

#### K8s manifest files 
* mongo-config.yaml
* mongo-secret.yaml
* mongo.yaml
* webapp.yaml

#### K8s commands

##### get basic info about k8s components
    kubectl get node
    kubectl get pod
    kubectl get svc
    kubectl get all

##### get extended info about components
    kubectl get pod -o wide
    kubectl get node -o wide

##### get detailed info about a specific component
    kubectl describe svc {svc-name}
    kubectl describe pod {pod-name}

##### get application logs
    kubectl logs {pod-name}
 
 
 docker-compose -f ..\..\docker-compose.yml build

kubectl config use-context docker-for-desktop

kubectl delete secret namespaceOfRepo.secret.local
kubectl create secret generic namespaceOfRepo.secret.local --from-env-file=.secrets

kubectl apply -f . ? how to and what is best practice

docker-compose -f ..\..\docker-compose.yml build

kubectl config use-context docker-for-desktop

kubectl delete secret namespaceOfRepo.secret.local
kubectl create secret generic namespaceOfRepo.secret.local --from-env-file=.secrets

kubectl apply -f .

in order : 
#!/bin/bash

kubectl apply \
    -f ./namespace.yaml \
    -f ./dapr-config.yaml \
    -f ./secrets.yaml \
    -f ./seq.yaml \
    -f ./zipkin.yaml \
    -f ./sqldata.yaml \
    -f ./rabbitmq.yaml \
    -f ./redis.yaml \
    -f ./identity.yaml \
    -f ./apigateway.yaml \
    -f ./components/pubsub-rabbitmq.yaml \
    -f ./components/statestore.yaml \
    -f ./components/sendmail.yaml \
    -f ./catalog.yaml \
    -f ./ordering.yaml \
    -f ./basket.yaml \
    -f ./payment.yaml \
    -f ./webshoppingagg.yaml \
    -f ./webspa.yaml \
    -f ./webstatus.yaml
