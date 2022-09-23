#  "Kubernetes Practice"

This is a simple Kubernetes implementation of 2 different service with a custom docker image

NodeJs backend that will interact with user (Type loadbalancer)

Nginx that will be called from the NodeJs service(ClusterIP)

# Create alias 
    alias k="kubectl"


## Create Kubernetes deployment & service (Seperate)
    k apply -f service.yaml 
    k apply -f deployment.yaml 

## Create Kubernetes deployment & service (Combine)
    k apply -f k8s-web-to-nginx.yaml -f nginx.yaml


# Delete service & deployment 
    k delete -f nginx.yaml -f k8s-web-to-nginx.yaml 


# Access web portal 
    minikube service k8s-web-to-nginx
    
# Nginx web portal route
    /nginx

