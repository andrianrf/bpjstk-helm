BPJSTK Multichannel Payment Gateway is an application that can communicate with the BPJSTK payment api, as well as being able to process debits and credits to the core banking banking system.

This application consists of several services, namely:
1. oracle-db: database for bpjstk-service
2. bpjstk-simulator: BPJSTK fire simulator service for testing.
3. iso-server : banking core banking simulator service
4. iso-client: connecting service to core banking banking
5. bpjstk-service: main service BPJSTK Payment Gateway
6. backoffice : interface for monitoring bpjstk-service
7. backoffice-be : backend interface backoffice

Following are the steps to run this service :
kubectl create namespace bpjstk-service
helm repo add bpjstk-service https://andrianrf.github.io/bpjstk-helm/charts/
helm install bpjstk-service . --namespace=bpjstk-service --values https://andrianrf.github.io/bpjstk-helm/values.yaml

