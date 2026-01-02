# PRACTICAL TEST – SET B

**Exam Type:** 100% Hands-on / Practical  
**Duration:** 2 Hours (120 Minutes)  
**Total Marks:** 100  

---

## Platforms Covere
- Red Hat RHEL 9 (RHCSA)
- Amazon Web Services (AWS)
- HashiCorp Terraform
- Git & GitHub
- Podman

---

##  SECTION A: RHCSA (RHEL 9) – 30 MARKS

### Task A1: Users, Groups & Sudo (10 Marks)
1. Create a group named `ops`
2. Create a user `student1`
3. Configure the following:
   - Home directory: `/opt/student1`
   - Login shell: `/bin/bash`
4. Add `student1` to the `ops` group
5. Configure sudo so `student1` can restart the `httpd` service **without password**

---

### Task A2: File Permissions & ACL (10 Marks)
1. Create directory `/shared/projects`
2. Set:
   - Owner: `root`
   - Group: `ops`
3. Permissions:
   - Owner: full access
   - Group: read/write
   - Others: no access
4. Configure **default ACL** so new files inherit group write permission

---

### Task A3: Storage & Swap (10 Marks)
1. Create a logical volume named `lv_swap` of size **512MB**
2. Format the logical volume as swap
3. Enable swap immediately
4. Ensure swap is enabled automatically after reboot

---

##  SECTION B: AWS – 20 MARKS

### Task B1: EC2 + EBS
1. Launch an EC2 instance:
   - OS: Amazon Linux 2
   - Instance type: `t2.micro`
2. Create a **5 GB EBS volume**
3. Attach the EBS volume to the EC2 instance
4. Format and mount it at `/mnt/data`
5. Ensure the mount persists after reboot

---

##  SECTION C: TERRAFORM – 20 MARKS

### Task C1: Terraform Resource Management
1. Write Terraform configuration to:
   - Create an S3 bucket
   - Enable versioning on the bucket
2. Use variables for:
   - Bucket name
   - AWS region
3. Output the bucket name
4. Execute the following commands:
   ```bash
   terraform init
   terraform validate
   terraform apply
   ```
##  SECTION D: GIT & GITHUB – 15 MARKS

### Task D1: Git Version Control
1. Initialize a Git repository named `infra-lab`
2. Add Terraform configuration files to the repository
3. Commit the changes with the message: `Add initial infrastructure code`
4. Create a branch named `feature`
5. Add a new file named `notes.txt`
6. Commit the changes
7. Merge the `feature` branch into the `main` branch
8. Push the repository to GitHub

---

##  SECTION E: CONTAINERS (PODMAN / DOCKER) – 15 MARKS

### Task E1: Container Management
1. Pull the `httpd` image using **Podman**
2. Run a container with the following configuration:
- Container name: `webserver`
- Port mapping: `9090:80`
3. Configure the container to start automatically on system reboot
4. Verify container access using: `curl http://localhost:9090`
