# helm-charts

[![Artifact HUB](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/secret-manager)](https://artifacthub.io/packages/helm/secret-manager/secret-manager)

## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

# Application Access Guide (Beta Version)

Welcome to the application access guide! This is a **beta version** currently under development. Please follow the steps below to set up and access the application.

---

## How to access the Application

1. **Port Forward Configuration**  
   To access the services directly, run the following command in your terminal:
   ```bash
   kubectl port-forward svc/frontend 3000:3000 & kubectl port-forward svc/backend 8080:8080

2. **Authentication**  
    Use the following credentials to log in to the application:
    ```bash
    Username: admin
    Password: admin

## Deploying the Application with NGINX Ingress Controller

If you want better integrate the application into a Kubernetes cluster, consider using the NGINX Ingress Controller. This approach allows the services to be exposed via HTTP/HTTPS endpoints, making them accessible using defined hostnames.

### Benefits of Using an Ingress Controller
1. Simplifies the management of HTTP and HTTPS traffic.
2. Supports routing requests to multiple services based on hostname or path.
3. Provides features like TLS termination, request redirection, and load balancing.


### Using the NGINX Ingress Controller

The NGINX Ingress Controller can be deployed in the Kubernetes cluster using tools like Helm or kubectl. After deployment:

1. Define Ingress rules to route traffic to the appropriate services (e.g., frontend and backend).
2. Map hostnames (e.g., frontend.example.com, backend.example.com) to the Ingress resources for external access.
3. Use DNS or update your local /etc/hosts file to resolve the hostnames.