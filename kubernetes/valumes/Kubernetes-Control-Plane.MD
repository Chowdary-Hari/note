## **Kubernetes Control Plane**
# Master node
### **1. etcd Cluster**
- **What it is**: A distributed key-value store.
- **Purpose**: Stores all cluster configuration and state, including nodes, pods, and secrets.
- **Why it matters**: It ensures consistency across the cluster.

### **2. Kube Scheduler**
- **What it is**: A component that assigns workloads (pods) to nodes.
- **Purpose**: Decides the best node for a pod based on resource availability and policies.
- **Why it matters**: Ensures efficient resource utilization and workload distribution.

### **3. Kube Controllers Manager**
- **What they are**: Background processes that handle different tasks in the cluster.
  - **Types of Controllers**:

    | Controller Name                  | Purpose                                                 |
    |----------------------------------|---------------------------------------------------------|
    | **Node Controller**              | Monitors node health & removes failed nodes.            |
    | **Replication Controller**       | Ensures the correct number of pod replicas are running. |
    | **Endpoint Controller**          | Updates Service & Endpoint objects when pods change.    |
    | **Service Account Controller**   | Manages default service accounts for new namespaces.    |
    | **Job Controller**               | Ensures that jobs complete successfully.                |
    | **Persistent Volume Controller** | Manages storage volumes for pods.                       |

---


### **4. Kube API Server**
- **What it is**: The main communication hub of Kubernetes.
- **Purpose**: Handles requests from users, CLI tools (kubectl), and other components.
- **Why it matters**: It ensures all actions (like deploying applications) are processed correctly.

# Worker node

### **Kubelet** → 
- Communicates with API Server & manages containers.
### **Kube Proxy** →
- Handles networking & service communication.
### **Container Runtime Engine** → 
- Runs containers (Docker, containerd, etc.).