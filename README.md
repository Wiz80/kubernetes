<p align="center">
  <img src="https://raw.githubusercontent.com/PKief/vscode-material-icon-theme/ec559a9f6bfd399b82bb44393651661b08aaf7ba/icons/folder-markdown-open.svg" width="100" alt="project-logo">
</p>
<p align="center">
    <h1 align="center">Kubernetes</h1>
</p>
<p align="center">
    <em>Empowering pods, scaling success within Kubernetes.</em>
</p>
<p align="center">
	<img src="https://img.shields.io/github/license/Wiz80/kubernetes?style=default&logo=opensourceinitiative&logoColor=white&color=0080ff" alt="license">
	<img src="https://img.shields.io/github/last-commit/Wiz80/kubernetes?style=default&logo=git&logoColor=white&color=0080ff" alt="last-commit">
	<img src="https://img.shields.io/github/languages/top/Wiz80/kubernetes?style=default&color=0080ff" alt="repo-top-language">
	<img src="https://img.shields.io/github/languages/count/Wiz80/kubernetes?style=default&color=0080ff" alt="repo-language-count">
<p>
<p align="center">
	<!-- default option, no dependency badges. -->
</p>

<br><!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary><br>

- [ Overview](#-overview)
- [ Features](#-features)
- [ Repository Structure](#-repository-structure)
- [ Modules](#-modules)
- [ Getting Started](#-getting-started)
  - [ Installation](#-installation)
  - [ Usage](#-usage)
  - [ Tests](#-tests)
- [ Project Roadmap](#-project-roadmap)
- [ Contributing](#-contributing)
- [ License](#-license)
- [ Acknowledgments](#-acknowledgments)
</details>
<hr>

##  Overview

The project, utilizing Kubernetes, orchestrates a variety of essential functionalities such as defining health probes, implementing ConfigMaps for configuration management, deploying services with Ingress rules, setting resource limits, managing namespaces, and establishing pods with multiple containers. It enhances Kubernetes architecture by enabling seamless deployment, scaling, monitoring, and resource optimization for various applications. This project, named K8sOpsKit, simplifies the management and maintenance of containerized environments, contributing significantly to streamlined operations within Kubernetes clusters.

---

##  Features

|    |   Feature         | Description |
|----|-------------------|---------------------------------------------------------------|
| ⚙️  | **Architecture**  | The project follows a modular architecture, utilizing Kubernetes resources like ConfigMaps, Deployments, Services, and Pods effectively. It demonstrates best practices for scalable and maintainable Kubernetes deployments. |
| 🔩 | **Code Quality**  | The codebase maintains a high level of quality with clear naming conventions, consistent formatting, and adherence to Kubernetes best practices. It includes comments and documentation within the code for easy understanding. |
| 📄 | **Documentation** | Extensive documentation is available for various components like ConfigMaps, Ingress, Namespaces, Pods, Services, etc. The documentation provides detailed explanations, examples, and best practices for configuring and deploying applications in a Kubernetes environment. |
| 🔌 | **Integrations**  | The project integrates with essential Kubernetes resources like Nginx, Ingress, ConfigMaps, and Services. These integrations enable seamless deployment, scaling, and networking within a Kubernetes cluster. |
| 🧩 | **Modularity**    | The codebase is highly modular, with components organized into separate directories based on functionality. This modularity enhances code reusability and maintainability, allowing for easy customization and extension of Kubernetes deployments. |
| 🧪 | **Testing**       | Testing frameworks and tools are not explicitly mentioned in the repository contents. Suggest implementing testing frameworks like Kubernetes Test Framework to ensure the reliability and robustness of the deployment configurations. |
| ⚡️  | **Performance**   | The project demonstrates efficient resource usage and scalability through defined resource quotas, limits, and scalable deployments. These practices ensure optimal performance and resource utilization within the Kubernetes environment. |
| 🛡️ | **Security**      | Security measures like namespace segregation and resource quotas are implemented to control access and resource allocation. However, further security enhancements like RBAC and network policies could be beneficial for enhancing data protection and access control. |
| 📦 | **Dependencies**  | Key external dependencies include Nginx, YAML configurations, HTML files, and configuration files for defining Kubernetes resources like ConfigMaps, Deployments, Services, and Ingress. These dependencies facilitate application configuration and deployment in Kubernetes. |

---

##  Repository Structure

```sh
└── kubernetes/
    ├── README.md
    ├── configmaps
    │   ├── cm-nginx-env.yaml
    │   ├── cm-nginx-vol.yaml
    │   └── configmaps-examples
    ├── deployment
    │   └── dep.yaml
    ├── envs
    │   └── env.yaml
    ├── health-probes
    │   ├── liveness-TCP.yaml
    │   ├── liveness-cmd.yaml
    │   └── liveness-http.yaml
    ├── ingress
    │   ├── app-ingress2.yaml
    │   ├── ingress-dep.yaml
    │   ├── ingress-rules.yaml
    │   ├── minikube-darwin-arm64
    │   └── nginx-controller.yaml
    ├── limitRange
    │   └── default-cpu-mem.yaml
    ├── limits-request
    │   ├── lim-cpu.yaml
    │   └── lim-ram.yaml
    ├── namespaces
    │   ├── backend.yaml
    │   ├── ns.yaml
    │   └── ns2.yaml
    ├── pods
    │   ├── 2containers.yaml
    │   ├── labels.yaml
    │   └── pod.yaml
    ├── replicaset
    │   └── rs.yaml
    ├── resourceQuota
    │   └── rq.yaml
    └── services
        ├── nodeport.yaml
        └── services.yaml
```

---

##  Modules

<details closed><summary>health-probes</summary>

| File                                                                                                   | Summary                                                                                                                                                                                                                                         |
| ---                                                                                                    | ---                                                                                                                                                                                                                                             |
| [liveness-TCP.yaml](https://github.com/Wiz80/kubernetes/blob/master/health-probes/liveness-TCP.yaml)   | Defines liveness check for goproxy Pod to ensure continuous operation by probing port 8080. Delivers crucial monitoring and ensures seamless functionality within the Kubernetes infrastructure.                                                |
| [liveness-cmd.yaml](https://github.com/Wiz80/kubernetes/blob/master/health-probes/liveness-cmd.yaml)   | Defines a liveness probe for a Kubernetes pod, ensuring continuous availability. Executes a command to check the health status, triggering actions based on the results. Critical for monitoring and maintaining pod health within the cluster. |
| [liveness-http.yaml](https://github.com/Wiz80/kubernetes/blob/master/health-probes/liveness-http.yaml) | Defines a Pod with an HTTP liveness probe for the Kubernetes cluster. Monitors Pod health by sending HTTP requests to /healthz endpoint. Eases identifying and recovering from unhealthy Pod states.                                            |

</details>

<details closed><summary>configmaps</summary>

| File                                                                                              | Summary                                                                                                                                                                                                                                              |
| ---                                                                                               | ---                                                                                                                                                                                                                                                  |
| [cm-nginx-vol.yaml](https://github.com/Wiz80/kubernetes/blob/master/configmaps/cm-nginx-vol.yaml) | Implements ConfigMap-based nginx configuration, Deployment, and NodePort Service for nginx app in the repository. ConfigMap defines nginx settings, Deployment uses it for nginx configuration, and the Service exposes the app on a specified port. |
| [cm-nginx-env.yaml](https://github.com/Wiz80/kubernetes/blob/master/configmaps/cm-nginx-env.yaml) | Implements nginx server configuration and database connection in Kubernetes. ConfigMaps define nginx settings and db credentials. Deployment uses ConfigMaps for environment variables and volumes. Service exposes nginx on specified port.         |

</details>

<details closed><summary>configmaps.configmaps-examples</summary>

| File                                                                                                    | Summary                                                                                                                                                                                                              |
| ---                                                                                                     | ---                                                                                                                                                                                                                  |
| [index.html](https://github.com/Wiz80/kubernetes/blob/master/configmaps/configmaps-examples/index.html) | Illustrates usage examples for configmaps in Kubernetes, showcasing best practices for managing configuration data. Essential resource for developers configuring applications in a Kubernetes environment.          |
| [nginx.conf](https://github.com/Wiz80/kubernetes/blob/master/configmaps/configmaps-examples/nginx.conf) | Defines Nginx server config for handling web traffic to localhost on port 8080, serving static content from /usr/share/nginx/html. Includes error page handling. Key for configuring Nginx in Kubernetes deployment. |

</details>

<details closed><summary>ingress</summary>

| File                                                                                                   | Summary                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ---                                                                                                    | ---                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [app-ingress2.yaml](https://github.com/Wiz80/kubernetes/blob/master/ingress/app-ingress2.yaml)         | Deploys API server with 3 replicas using Nginx image. Exposes on port 9090 with a NodePort service. Supports dynamic content updates. Contributing to the Kubernetes architecture with ingress functionality.                                                                                                                                                                                                                                                                                                                                                         |
| [ingress-rules.yaml](https://github.com/Wiz80/kubernetes/blob/master/ingress/ingress-rules.yaml)       | Defines routing rules for Ingress to direct traffic based on URL paths to different backend services within the Kubernetes cluster.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [ingress-dep.yaml](https://github.com/Wiz80/kubernetes/blob/master/ingress/ingress-dep.yaml)           | Depicts Deployment and Service for Nginx app, proficiently orchestrating its scaling and network accessibility. Strategically aligns with Kubernetes structure for effective app deployment and service exposure.                                                                                                                                                                                                                                                                                                                                                     |
| [nginx-controller.yaml](https://github.com/Wiz80/kubernetes/blob/master/ingress/nginx-controller.yaml) | This code file, `dep.yaml` in the `deployment` directory, plays a crucial role in the repositorys architecture by defining the deployment specifications for a particular component or service within a Kubernetes cluster. It outlines the desired state of the deployment, including the container images to be used, resource limits, replica counts, and other configuration parameters. This file serves as a blueprint for orchestrating the deployment process, ensuring that the application runs smoothly and efficiently within the Kubernetes environment. |

</details>

<details closed><summary>limits-request</summary>

| File                                                                                        | Summary                                                                                                                                                                                                                                             |
| ---                                                                                         | ---                                                                                                                                                                                                                                                 |
| [lim-ram.yaml](https://github.com/Wiz80/kubernetes/blob/master/limits-request/lim-ram.yaml) | Defines memory limits and requests for a Pod named memory-demo. Specifies resource thresholds for memory and CPU allocation, using the polinux/stress image to stress-test memory.                                                                  |
| [lim-cpu.yaml](https://github.com/Wiz80/kubernetes/blob/master/limits-request/lim-cpu.yaml) | Defines memory and CPU limits for the memory-demo pod, ensuring stable resource allocation when running the stress command with specified arguments. This configuration enhances resource utilization efficiency within the Kubernetes environment. |

</details>

<details closed><summary>namespaces</summary>

| File                                                                                    | Summary                                                                                                                                                                                                                                                                                          |
| ---                                                                                     | ---                                                                                                                                                                                                                                                                                              |
| [ns.yaml](https://github.com/Wiz80/kubernetes/blob/master/namespaces/ns.yaml)           | Defines a Kubernetes namespace named development with relevant metadata labels. Situates the namespace within the repository's architecture to segregate resources based on their purpose.                                                                                                       |
| [backend.yaml](https://github.com/Wiz80/kubernetes/blob/master/namespaces/backend.yaml) | Defines a Kubernetes namespace ci with a backend Deployment and Service. Ensures three backend replicas, networking via NodePort, and labels for identification. Integrates images from harry2680/backend-k8s-hands-on for seamless deployment and scaling within the repository's architecture. |
| [ns2.yaml](https://github.com/Wiz80/kubernetes/blob/master/namespaces/ns2.yaml)         | Defines namespaces for dev and prod environments. Deploys an Nginx app with different replicas based on the environment for isolation and scaling. Contributes to segregating resources efficiently within Kubernetes cluster.                                                                   |

</details>

<details closed><summary>pods</summary>

| File                                                                                      | Summary                                                                                                                                                                                                                                           |
| ---                                                                                       | ---                                                                                                                                                                                                                                               |
| [labels.yaml](https://github.com/Wiz80/kubernetes/blob/master/pods/labels.yaml)           | Defines Pod labels for nginx2 and nginx3 instances under app and env categories. Categorizes instances as front/dev and backend/prod. Facilitates resource identification and management within the Kubernetes cluster architecture.              |
| [2containers.yaml](https://github.com/Wiz80/kubernetes/blob/master/pods/2containers.yaml) | Implements a Pod with two containers running Python servers, each serving different content on port 8082. This file enhances the Kubernetes architecture by supporting multi-container Pods for increased functionality and resource utilization. |
| [pod.yaml](https://github.com/Wiz80/kubernetes/blob/master/pods/pod.yaml)                 | Defines two NGINX Pods with container specifications, facilitating deployment configurations for NGINX services within Kubernetes pods.                                                                                                           |

</details>

<details closed><summary>resourceQuota</summary>

| File                                                                             | Summary                                                                                                                                                                                                                               |
| ---                                                                              | ---                                                                                                                                                                                                                                   |
| [rq.yaml](https://github.com/Wiz80/kubernetes/blob/master/resourceQuota/rq.yaml) | Defines resource quotas for high-priority pods within the uid namespace, specifying CPU and memory limits. Maintains resource allocation control by capping pod count, CPU requests, and memory usage for optimal system performance. |

</details>

<details closed><summary>deployment</summary>

| File                                                                            | Summary                                                                                                                                                                                                                          |
| ---                                                                             | ---                                                                                                                                                                                                                              |
| [dep.yaml](https://github.com/Wiz80/kubernetes/blob/master/deployment/dep.yaml) | Implements a deployment configuration for Nginx with service connectivity. Orchestrates three Nginx replicas, each running on port 80, and exposes a service on port 8080 for frontend access within the Kubernetes environment. |

</details>

<details closed><summary>limitRange</summary>

| File                                                                                                    | Summary                                                                                                                                                                                               |
| ---                                                                                                     | ---                                                                                                                                                                                                   |
| [default-cpu-mem.yaml](https://github.com/Wiz80/kubernetes/blob/master/limitRange/default-cpu-mem.yaml) | Defines default CPU and memory limits for containers in the dev namespace. Ensures each container has specified resource restrictions for CPU and memory when deployed in the Kubernetes environment. |

</details>

<details closed><summary>replicaset</summary>

| File                                                                          | Summary                                                                                                                                                                                            |
| ---                                                                           | ---                                                                                                                                                                                                |
| [rs.yaml](https://github.com/Wiz80/kubernetes/blob/master/replicaset/rs.yaml) | Defines a ReplicaSet managing two Python containers for scalable frontend tier. Maintains consistency with the repositorys Kubernetes architecture by using specified labels and container images. |

</details>

<details closed><summary>envs</summary>

| File                                                                      | Summary                                                                                                                                                                                                                                     |
| ---                                                                       | ---                                                                                                                                                                                                                                         |
| [env.yaml](https://github.com/Wiz80/kubernetes/blob/master/envs/env.yaml) | Demonstrates a Pod configuration with environmental variables. Named envar-demo, it uses Nginx image to showcase setting variables like GREETING and FAREWELL for a clear learning purpose within the repository's Kubernetes architecture. |

</details>

<details closed><summary>services</summary>

| File                                                                                    | Summary                                                                                                                                                                                      |
| ---                                                                                     | ---                                                                                                                                                                                          |
| [services.yaml](https://github.com/Wiz80/kubernetes/blob/master/services/services.yaml) | Defines a deployment with 3 replicas of nginx containers and a service exposing port 8080 mapped to port 80 for the front app in the Kubernetes repository.                                  |
| [nodeport.yaml](https://github.com/Wiz80/kubernetes/blob/master/services/nodeport.yaml) | Implements a NodePort service and deployment for backend applications, ensuring availability and load balancing. Syncs service endpoints to pods running the nginx container on TCP port 80. |

</details>

---

##  Getting Started

**System Requirements:**

* **YAML**: `version x.y.z`

###  Installation

<h4>From <code>source</code></h4>

> 1. Clone the kubernetes repository:
>
> ```console
> $ git clone https://github.com/Wiz80/kubernetes
> ```
>
> 2. Change to the project directory:
> ```console
> $ cd kubernetes
> ```
>
> 3. Install the dependencies:
> ```console
> $ > INSERT-INSTALL-COMMANDS
> ```

###  Usage

<h4>From <code>source</code></h4>

> Run kubernetes using the command below:
> ```console
> $ > INSERT-RUN-COMMANDS
> ```

###  Tests

> Run the test suite using the command below:
> ```console
> $ > INSERT-TEST-COMMANDS
> ```

---

##  Project Roadmap

- [X] `► INSERT-TASK-1`
- [ ] `► INSERT-TASK-2`
- [ ] `► ...`

---

##  Contributing

Contributions are welcome! Here are several ways you can contribute:

- **[Report Issues](https://github.com/Wiz80/kubernetes/issues)**: Submit bugs found or log feature requests for the `kubernetes` project.
- **[Submit Pull Requests](https://github.com/Wiz80/kubernetes/blob/main/CONTRIBUTING.md)**: Review open PRs, and submit your own PRs.
- **[Join the Discussions](https://github.com/Wiz80/kubernetes/discussions)**: Share your insights, provide feedback, or ask questions.

<details closed>
<summary>Contributing Guidelines</summary>

1. **Fork the Repository**: Start by forking the project repository to your github account.
2. **Clone Locally**: Clone the forked repository to your local machine using a git client.
   ```sh
   git clone https://github.com/Wiz80/kubernetes
   ```
3. **Create a New Branch**: Always work on a new branch, giving it a descriptive name.
   ```sh
   git checkout -b new-feature-x
   ```
4. **Make Your Changes**: Develop and test your changes locally.
5. **Commit Your Changes**: Commit with a clear message describing your updates.
   ```sh
   git commit -m 'Implemented new feature x.'
   ```
6. **Push to github**: Push the changes to your forked repository.
   ```sh
   git push origin new-feature-x
   ```
7. **Submit a Pull Request**: Create a PR against the original project repository. Clearly describe the changes and their motivations.
8. **Review**: Once your PR is reviewed and approved, it will be merged into the main branch. Congratulations on your contribution!
</details>

<details closed>
<summary>Contributor Graph</summary>
<br>
<p align="center">
   <a href="https://github.com{/Wiz80/kubernetes/}graphs/contributors">
      <img src="https://contrib.rocks/image?repo=Wiz80/kubernetes">
   </a>
</p>
</details>

---

##  License

This project is protected under the [SELECT-A-LICENSE](https://choosealicense.com/licenses) License. For more details, refer to the [LICENSE](https://choosealicense.com/licenses/) file.

---

##  Acknowledgments

- List any resources, contributors, inspiration, etc. here.

[**Return**](#-overview)

---
