# PRACTICAL HANDS-ON TEST 
---

##  SECTION A: RHEL SYSTEM ADMINISTRATION (45 Marks)

### Task A1: User & Group Management (10 Marks)

1. Create a group named:

   ```
   cloudops
   ```

2. Create users:

   ```
   alice
   bob
   ```

3. Conditions:

   * Both users must belong to `cloudops`
   * Set passwords for both users
   * Expire password of `bob` after first login

4. Verify:

   ```
   id alice
   chage -l bob
   ```

---

### Task A2: File Permissions & Ownership (10 Marks)

1. Create directory:

   ```
   /srv/project
   ```

2. Set:

   * Owner: root
   * Group: cloudops
   * Permissions:

     * Owner: full access
     * Group: read/write
     * Others: no access

3. Create file:

   ```
   /srv/project/info.txt
   ```

4. Test access using user `alice`.

---

### Task A3: Systemd Basic Service (10 Marks)

1. Create script:

   ```
   /usr/local/bin/disk-check.sh
   ```

2. Script should log disk usage of `/` into:

   ```
   /var/log/disk-check.log
   ```

3. Create systemd service:

   ```
   disk-check.service
   ```

4. Enable and start the service.

---

### Task A4: Cron Job & Archiving (10 Marks)

1. Create script:

   ```
   /usr/local/bin/home-backup.sh
   ```

2. Compress `/home/alice` into:

   ```
   /backup/alice-<date>.tar.gz
   ```

3. Schedule cron job:

   * Runs daily at **2:00 AM**

---

### Task A5: Disk & Mount Management (5 Marks)

1. Create directory:

   ```
   /data
   ```

2. Mount an existing partition permanently using `/etc/fstab`.

3. Verify mount after reboot.

---

##  SECTION B: GIT VERSION CONTROL (30 Marks)

### Task B1: Basic Git Workflow (10 Marks)

1. Initialize Git repository:

   ```
   linux-cloud-lab
   ```

2. Create files:

   ```
   README.md
   notes.txt
   ```

3. Commit with message:

   ```
   Initial commit
   ```

---

### Task B2: Branching & Merge (10 Marks)

1. Create branch:

   ```
   dev
   ```

2. Modify `notes.txt`.

3. Commit changes.

4. Merge `dev` into `main`.

---

### Task B3: Undo & Recovery (10 Marks)

1. Delete `notes.txt`.
2. Commit the deletion.
3. Restore `notes.txt` from Git history.
4. Verify file restoration.

---

## SECTION C: TERRAFORM BASICS (35 Marks)

### Task C1: Terraform Setup (10 Marks)

1. Install Terraform.

2. Verify installation:

   ```
   terraform version
   ```

3. Create directory:

   ```
   terraform-lab
   ```

---

### Task C2: Simple AWS Resource (15 Marks)

1. Configure AWS provider:

   * Region: `ap-south-1`

2. Create:

   * One EC2 instance
   * Instance type: `t2.micro`

3. Use Terraform variables for:

   * Region
   * Instance type

4. Execute:

   ```
   terraform init
   terraform plan
   terraform apply
   ```

---

### Task C3: Outputs & Destroy (10 Marks)

1. Create outputs for:

   * EC2 Instance ID
   * Public IP

2. Destroy infrastructure:

   ```
   terraform destroy
   ```

---

##  SECTION D: AWS BASIC OPERATIONS (30 Marks)

### Task D1: IAM User Creation (10 Marks)

1. Create IAM user:

   ```
   dev-user
   ```

2. Attach policy:

   * EC2 ReadOnlyAccess

3. Configure AWS CLI on RHEL system.

4. Verify:

   ```
   aws ec2 describe-instances
   ```

---

### Task D2: S3 Basics (10 Marks)

1. Create S3 bucket:

   ```
   simple-backup-<yourname>
   ```

2. Upload a file using AWS CLI.

3. Verify upload using AWS Console or CLI.

---

### Task D3: EC2 Verification (10 Marks)

1. SSH into EC2 instance.
2. Run:

   ```
   hostname
   uptime
   ```
```
df -h

```

---

## SECTION E: SIMPLE INTEGRATED TASK (10 Marks)

### Task E1: Git + Terraform Integration (10 Marks)

1. Store Terraform code in a Git repository.
2. Push repository to GitHub.
3. Clone repository on another system.
4. Run Terraform successfully from cloned repo.

---

## 🏁 FINAL VALIDATION COMMANDS

```

id alice
systemctl status disk-check
crontab -l
git log --oneline
terraform plan
aws s3 ls

```

---

##  END OF PRACTICAL TEST

```
