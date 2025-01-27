### **1. Install Terraform on Linux**

#### **Step 1: Update Your Package List**
Run the following command to update your system's package list:
```bash
sudo apt-get update
```

#### **Step 2: Install Dependencies**
Install required dependencies like `wget` or `curl` if they are not already installed:
```bash
sudo apt-get install -y wget unzip
```

#### **Step 3: Download Terraform Binary**
Go to the official Terraform download page: [https://www.terraform.io/downloads](https://www.terraform.io/downloads).  
Or, use this command to download the latest version (replace `VERSION` with the desired version):
```bash
wget https://releases.hashicorp.com/terraform/<VERSION>/terraform_<VERSION>_linux_amd64.zip
```
For example:
```bash
wget https://releases.hashicorp.com/terraform/1.6.0/terraform_1.6.0_linux_amd64.zip
```

#### **Step 4: Extract the Binary**
Unzip the downloaded file:
```bash
unzip terraform_<VERSION>_linux_amd64.zip
```

#### **Step 5: Move Terraform to a System Path**
Move the `terraform` binary to a directory in your system's PATH:
```bash
sudo mv terraform /usr/local/bin/
```

#### **Step 6: Verify the Installation**
Check if Terraform is successfully installed:
```bash
terraform version
```
You should see the installed version of Terraform.

---

### **2. Install Terraform on macOS**

#### **Step 1: Install Homebrew (if not already installed)**
If you don’t have Homebrew installed, install it first:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### **Step 2: Install Terraform**
Use Homebrew to install Terraform:
```bash
brew tap hashicorp/tap
brew install hashicorp/tap/terraform
```

#### **Step 3: Verify the Installation**
Check the installed version of Terraform:
```bash
terraform version
```

---

### **3. Install Terraform on Windows**

#### **Step 1: Download Terraform**
Visit the Terraform downloads page: [https://www.terraform.io/downloads](https://www.terraform.io/downloads).  
Download the appropriate `.zip` file for Windows (64-bit).

#### **Step 2: Extract the File**
Extract the `.zip` file into a folder of your choice (e.g., `C:\Terraform`).

#### **Step 3: Add Terraform to the PATH**
1. Search for "Environment Variables" in the Windows search bar.
2. Under "System Properties," click **Environment Variables**.
3. In the **System Variables** section, find the `Path` variable and click **Edit**.
4. Click **New**, and add the path to the Terraform folder (e.g., `C:\Terraform`).
5. Click **OK** to save the changes.

#### **Step 4: Verify the Installation**
Open a new Command Prompt or PowerShell window and check the Terraform version:
```powershell
terraform version
```

---

### **Optional Step: Set Up Terraform in GitHub Codespaces** 

refer codespace.md for steps
