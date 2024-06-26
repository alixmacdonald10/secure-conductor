<p align="center">
  <img align="center" width="33%" src="./docs/images/secure-conductor.png" >
</p>

# SecureConductor
SecureConductor is a tool designed to handle secret management within a Kubernetes environment. It ensures consistency in Kubernetes configurations across various platforms, allowing for platform-agnostic deployments.  

SecureConductor is deployed as a pod within its designated namespace in your Kubernetes cluster. It monitors the secret store of your chosen platform (such as Azure Keyvault, AWS Secrets Manager, etc.). It then retrieves secrets from the platform's secret store and deploys them as Kubernetes secrets within your cluster to X number of target namespaces. SecureConductor periodically checks the secret store for updates and automatically updates the corresponding Kubernetes secret accordingly. This process is shown below for clarity.

<p align="center">
  <img align="center" width="33%" src="./docs/images/basic-operation.png" >
</p>

### Additional Features
Additionally, SecureConductor offers the flexibility to be imported as a standalone library (secure-conductor-broker) into your existing Rust crate. This allows you to leverage its functionality solely for pulling secrets from various sources, streamlining integration into your project.

## Plaftorm Support
SecureConductor is compatible with the following platforms:

<!----> TODO: ADD pipeline test pass/fail to each platform
- Azure :x:
- AWS :x:
- GCP :x:
