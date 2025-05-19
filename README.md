TASK 5 

Title: Build a Kubernetes Cluster Locally with Minikube

Objective:

Deploy and manage containerized applications using Kubernetes. This task helps you understand how Kubernetes works locally using Minikube.

Tools Required:

- Minikube
- kubectl
- Docker

Steps:

1. Install Tools:
   a. Install Minikube:
      
2. Start Minikube Cluster:
   - Run: minikube start 
   - Verify: kubectl get nodes

3. Create Deployment:
   - Create a file named "deployment.yaml"
   
   - Apply the deployment:
     kubectl apply -f deployment.yaml

4. Expose the Deployment:
   - Create a file named "service.yaml"
 
   - Apply the service:
     kubectl apply -f service.yaml

   - Verify:
     kubectl get services

   - Access the app:
     minikube service nginx-service --url
     OR open http://localhost:30080 in your browser

5. Scale the Deployment:
   - To increase replicas:
     kubectl scale deployment mynginx-deployment --replicas=4

   - Verify:
     kubectl get pods

6. Debugging:
   - View pod status: kubectl get pods
   - Describe pod: kubectl describe pod <pod-name>
   - View logs: kubectl logs <pod-name>

Deliverables:

1. deployment.yaml
2. service.yaml
3. Screenshots of:
   - kubectl get pods
   - kubectl get services
   - App in browser (nginx page)
   - pod describe and logs
