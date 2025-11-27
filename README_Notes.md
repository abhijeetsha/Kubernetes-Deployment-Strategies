# Kubernetes-Deployment-Strategies
## ✅ What is Kubernetes Deployment?
### Ans: A Kubernetes Deployment is a high-level controller that manages Pods and ReplicaSets.
It ensures your application is running, scalable, up-to-date, and self-healing.

### Key functions of a Deployment:
* Creates and manages Pods via ReplicaSets
* Ensures the desired number of Pods always run
* Performs updates (rolling updates)
* Allows rollbacks if something goes wrong
* Supports scaling (manual or auto-scaling)

### In simple words:
* ➡️ Deployment is used to deploy, update, scale, and rollback containerized applications in Kubernetes.

## ✅ What are Kubernetes Deployment Strategies?
### Deployment strategies define how new application versions are released and how old versions are replaced.

## In simple terms:
### ➡️ It's the method Kubernetes uses to update your application without downtime (or with controlled downtime).

## 🔥 Super Short Summary Table
| Strategy       | Downtime | Short Explanation                |
| -------------- | -------- | -------------------------------- |
| Rolling Update | No       | Replace pods gradually           |
| Recreate       | Yes      | Delete old → create new          |
| Blue-Green     | No       | Two environments; switch traffic |
| Canary         | No       | Test on small % users            |
| A/B Testing    | No       | Traffic split by user group      |
| Shadow         | No       | Send traffic copy to new version |
| Partition      | No       | Update stateful apps in parts    |

## ✅ Types of Kubernetes Deployment Strategies (Short & Simple)
### 1️⃣ Rolling Update (Default)
* Gradually replaces old Pods with new Pods one-by-one → zero downtime.

### 2️⃣ Recreate
* Stops & deletes all old Pods first, then creates new Pods → downtime occurs.

### 3️⃣ Blue-Green Deployment
* Two environments (Blue = old, Green = new); switch traffic to Green when ready → safe & instant rollback.

### 4️⃣ Canary Deployment
* Releases new version to small % of users first; if stable, rollout to everyone → risk-free testing.

### 5️⃣ A/B Testing
* Routes traffic to different versions based on user segments (headers, cookies) → feature experimentation.

### 6️⃣ Shadow (Mirroring) Deployment
* New version receives real traffic copy but users don’t see responses → performance testing without impact.

### 7️⃣ Rolling with Partition (StatefulSets)
* Updates only part of the Pods; some Pods stay on old version → controlled, step-by-step rollout.
