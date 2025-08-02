K8s-mongoexpress-mondodb_stack Project

📘 README.md
📦 Kubernetes MongoDB + Mongo Express 
A full-featured Kubernetes deployment stack with MongoDB (StatefulSet), Mongo Express UI,  and TLS-enabled Ingress. Built for CKA-level lab practice and real-world DevOps workflows.

🚀 Features
✅ MongoDB ReplicaSet using StatefulSet + Headless Service
✅ Mongo Express UI via Deployment + Ingress
✅ TLS termination using cert-manager
✅ Internal ClusterIP & external Ingress with routing
✅ Secrets & ConfigMaps for secure config management
📽️ Demo
📁 GitHub Repo:https://github.com/GIRISHMESH/K8s-mongoexpress-mondodb_stack.git


🧰 Tech Stack
Kubernetes (kubectl, Minikube, or AKS)
MongoDB with Persistent Volumes
Mongo Express web client
Ingress-NGINX + cert-manager
GitHub Actions (optional for CI/CD)
📂 Folder Structure
manifests/
├── 01-namespace.yaml
├── 02-secret.yaml
├── 03-configmap.yaml
├── 04-storageclass.yaml
├── 05-mongodb-statefulset.yaml
├── 06-mongodb-headless-service.yaml
├── 07-mongodb-clusterip-service.yaml
├── 08-mongo-express-deployment.yaml
├── 09-mongo-express-service.yaml
├── 10-ingress.yaml
├── 11-replica-init-job.yaml
└── 12-network-policy.yaml

11-Deploy_in_order_commands
          
📦 Getting Started
🔧 Prerequisites
Kubernetes Cluster (Minikube, KIND, or AKS)
kubectl installed and configured
Optional: Helm, cert-manager, ingress-nginx controller
📥 Step-by-Step Deployment
# Clone the repository
git clone https://github.com/yourusername/mongo-k8s-stack.git
cd mongo-k8s-stack

# Start minikube (if using locally)
minikube start --driver=docker

# Apply all manifests
kubectl apply -f manifests/

# Check pods and services
kubectl get pods -n mongo-stack
kubectl get svc -n mongo-stack
kubectl get ingress -n mongo-stack
🔐 Security
All sensitive data (e.g., MongoDB credentials) is stored in Kubernetes Secrets
TLS via cert-manager ensures encrypted access through Ingress
📊 Monitoring with Prometheus
mongodb-exporter scrapes MongoDB metrics
Prometheus scrapes exporter and other pod metrics
Grafana dashboard integration possible
🧠 CKA Practice Scenarios Covered
StatefulSet + Headless Service setup
ConfigMaps & Secrets usage
Ingress + TLS configuration
Resource requests/limits
Monitoring & metrics integration
Job to initialize MongoDB Replica Set
📸 Screenshots
Add screenshots or terminal outputs of kubectl get pods, Prometheus UI, or Ingress response here if available.

📌 Notes
Default namespace: mongo-stack
PVC size: 10Gi (update as needed)
Ingress is assumed to be pre-installed with TLS enabled
You may customize domain names in 08-ingress.yaml
🙋‍♂️ Author
Girish Meshram 🔗 LinkedIn

📧 girimesh@gmail.com

⭐️ Star this repo

🔁 Fork it for your own use


