# iac-task3-docker-terraform
# ✅ Task 3: Docker Container Provisioning using Terraform

## 📌 Project Title:
**Provision a Docker Container using Terraform on Ubuntu 22.04 (EC2)**

---

## 🧱 Infrastructure Provisioned:

- 🔹 **Docker Image**: `nginx:latest`
- 🔹 **Docker Container**: 
  - Name: `my-nginx-container`
  - Exposed: Internal port `80` mapped to EC2 host port `8080`
- 🔹 Hosted on: AWS EC2 Instance (Ubuntu 22.04)

---

## 🔧 Tools Used:

- Terraform v1.x
- Docker Engine
- AWS EC2 (Ubuntu 22.04 LTS)

---

## 📁 Files Created:

```
terraform-docker-nginx/
├── main.tf               # Terraform configuration
├── execution_log.txt     # Terraform commands 
├── README.md             # Instructions, output, and setup guide
└── screenshots/          # (Optional) NGINX browser output
```

---

## 🚀 Terraform Execution Summary:

### ✅ Terraform Apply Output (Short View):
```
Apply complete! Resources: 2 added, 0 changed, 0 destroyed.
```

### 📄 Docker Container Running:
```
docker ps
```
```
CONTAINER ID   IMAGE          PORTS                    NAMES
abc123456789   nginx:latest   0.0.0.0:8080->80/tcp     my-nginx-container
```

### 📄 Terraform Resources Created:
```
terraform state list
```
```
docker_container.nginx
docker_image.nginx
```

---

## 🌐 NGINX Web Output:

**Browser**:  
> http://<EC2_PUBLIC_IP>:8080

✅ You will see the **NGINX Welcome Page**

**Curl from EC2**:
```
curl localhost:8080
```
Output:
```html
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
...
</html>
```

---

## 🧨 Terraform Destroy Output:

```
terraform destroy -auto-approve
```
```
Destroy complete! Resources: 2 destroyed.
```

---

## 📦 GitHub Repo Ready:

✅ Includes:
- Code (`main.tf`)
- Output log (`execution_log.txt`)
- Screenshot of NGINX
- README explaining the task

---

### 🏁 Final Status: **✅ Completed Successfully**
