# PRACTICAL TEST



## SECTION A: RHCSA (RHEL 9) 

### Task A1: User & Permissions 
1. Create a group named `devops`
2. Create a user `kubearc`
   - Primary group: `devops`
   - Home directory: `/data/kubearc`
3. Set password expiry to **90 days**
4. Allow `kubearc` to run `dnf` using sudo **without password**

---

### Task A2: Storage & Mounting 
1. Create a logical volume named `lv_practice` of size **500MB**
2. Format it using `xfs`
3. Mount it at `/practice`
4. Ensure the mount persists after reboot

---

### Task A3: Services & Firewall 
1. Install `httpd`
2. Start and enable the service
3. Allow HTTP service in the firewall
4. Verify the service is running

---

##  SECTION B: AWS – 20 MARKS

### Task B1: EC2 & Security Group
1. Launch an EC2 instance:
   - Amazon Linux 2
   - Instance type: `t2.micro`
2. Create a Security Group:
   - Allow SSH (port 22) from anywhere
3. Attach the Security Group to the instance
4. Verify SSH access

---

##  SECTION C: TERRAFORM – 20 MARKS

### Task C1: Infrastructure as Code
1. Write Terraform configuration to:
   - Create an EC2 instance
   - Create a Security Group allowing SSH
2. Use variables for:
   - AWS region
   - Instance type
3. Output the public IP of the EC2 instance
4. Run:
   - `terraform init`
   - `terraform plan`
   - `terraform apply`

---

## SECTION D: GIT & GITHUB 

### Task D1: Git Workflow
1. Create a Git repository named `kubearc-test`
2. Add Terraform files to the repository
3. Commit with message:
   ```
   Initial terraform setup
   ```
4. Create a branch named `test`
5. Modify the README file
6. Merge `test` branch into `main`
7. Push changes to GitHub

---

##  SECTION E: CONTAINERS (PODMAN / DOCKER) 

### Task E1: Container Deployment
1. Pull the `nginx` image using **Podman**
2. Run a container with:
- Name: `web`
- Port mapping: `8080:80`
3. Configure container to restart automatically
4. Verify using: *curl*


---

##  Evaluation Criteria
- Correct command execution
- Persistence after reboot (mounts, services)
- Terraform state file created
- Clean Git commit history
- Container accessible on port 8080

**Good Luck **
