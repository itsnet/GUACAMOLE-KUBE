
# 1. Install NGINX Ingress Controller
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v1.10.0/deploy/static/provider/cloud/deploy.yaml


# 2. Install Cert-Manager
kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.14.2/cert-manager.yaml

# 3. Configure Let's Encrypt Issuer
Create a ClusterIssuer for Let's Encrypt:
kubectl apply -f cluster-issuer.yaml

# 4. Deploy Your HTTP Website Pod and Service
kubectl apply -f http-pod-service.yaml

