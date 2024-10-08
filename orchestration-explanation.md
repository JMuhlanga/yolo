# Setup Instructions

---

## 1. Set Up Google Kubernetes Engine (GKE)

**1. Authenticate with Google Cloud:**

    gcloud auth login

**2. Set your project ID:**

    gcloud config set project yolo-ip4-orchestration

**3. Create a Kubernetes cluster:**

    gcloud container clusters create yolo-cluster --num-nodes=3 --zone=us-central1-a

**4. Get credentials for the cluster:**

    gcloud container clusters get-credentials yolo-cluster

---

## 2. Deploy MongoDB using StatefulSets

**1. Apply the MongoDB secret:**

    kubectl apply -f manifests/secrets/mongo-secrets.yaml

**2. Create the headless service for MongoDB:**

    kubectl apply -f manifests/headless-service/headless-service.yaml

**3. Deploy MongoDB StatefulSet:**

    kubectl apply -f manifests/statefulset/mongo-statefulset.yaml

---

## 3. Deploy Backend Service

**1. Deploy the backend:**

    kubectl apply -f manifests/deployment/backend-deployment.yaml

**2. Expose the backend service:**

    kubectl apply -f manifests/service/backend-service.yaml

---

## 4. Deploy Frontend Service

**1. Deploy the frontend:**

    kubectl apply -f manifests/deployment/frontend-deployment.yaml

**2. Expose the frontend service:**

    kubectl apply -f manifests/service/frontend-service.yaml

---

## 5. Verify the Deployment

**1. Check the status of your pods:**

    kubectl get pods

**2. Check the status of your services:**

    kubectl get services

---

## 6. Access Your Application

**Frontend Service:** The frontend service is exposed via a LoadBalancer. Get the external IP address with:

    kubectl get service yolo-frontend

Visit the external IP in your browser to access the frontend application.
