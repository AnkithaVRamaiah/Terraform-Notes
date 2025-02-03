# **Terraform commands** 
### 1. **`terraform init`**  
   - Initializes a Terraform working directory.
   - Downloads necessary provider plugins and sets up the backend (if configured).  
   - Must be run before any other Terraform commands.  
   - Example:  
     ```bash
     terraform init
     ```

### 2. **`terraform plan`**  
   - Creates an execution plan showing what changes Terraform will make.  
   - Helps preview modifications before applying them.  
   - Example:  
     ```bash
     terraform plan
     ```
   - To save the plan output to a file:  
     ```bash
     terraform plan -out=tfplan
     ```

### 3. **`terraform apply`**  
   - Applies the changes required to reach the desired state defined in `.tf` files.  
   - Prompts for approval before execution (unless `-auto-approve` is used).  
   - Example:  
     ```bash
     terraform apply
     ```
   - To apply a saved plan file:  
     ```bash
     terraform apply tfplan
     ```

### 4. **`terraform destroy`**  
   - Destroys all resources created by Terraform.  
   - Asks for confirmation before execution.  
   - Example:  
     ```bash
     terraform destroy
     ```
   - To bypass confirmation:  
     ```bash
     terraform destroy -auto-approve
     ```

### 5. **`terraform show`**  
   - Displays the current state or plan file output.  
   - Example:  
     ```bash
     terraform show
     ```
   - To view a specific plan file:  
     ```bash
     terraform show tfplan
     ```

### 6. **`terraform state`**  
   - Manages Terraform's state file (`terraform.tfstate`).  
   - Subcommands:
     - `terraform state list` → Lists all resources in the state.  
     - `terraform state show <resource>` → Shows details of a specific resource.  
     - `terraform state rm <resource>` → Removes a resource from the state file.  

### 7. **`terraform validate`**  
   - Validates the syntax and structure of Terraform configuration files.  
   - Example:  
     ```bash
     terraform validate
     ```

### 8. **`terraform fmt`**  
   - Formats Terraform configuration files to maintain consistency.  
   - Example:  
     ```bash
     terraform fmt
     ```

### 9. **`terraform output`**  
   - Displays values of output variables defined in Terraform.  
   - Example:  
     ```bash
     terraform output
     ```

### 10. **`terraform import`**  
   - Imports existing infrastructure into Terraform state.  
   - Example:  
     ```bash
     terraform import aws_instance.example i-1234567890abcdef0
     ```

### 11. **`terraform taint` (Deprecated in Terraform 1.0+)**  
   - Marks a resource for recreation during the next `terraform apply`.  
   - Example:  
     ```bash
     terraform taint aws_instance.example
     ```
   - In newer versions, use `terraform apply -replace="aws_instance.example"` instead.

### 12. **`terraform graph`**  
   - Generates a visual graph of the Terraform dependency tree.  
   - Example:  
     ```bash
     terraform graph | dot -Tpng > graph.png
     ```

### 13. **`terraform workspace`**  
   - Manages multiple workspaces (useful for managing different environments like dev, staging, prod).  
   - Example:  
     ```bash
     terraform workspace new dev
     terraform workspace select dev
     ```

### 14. **`terraform version`**  
   - Shows the Terraform version installed.  
   - Example:  
     ```bash
     terraform version
     ```

### 15. **`terraform providers`**  
   - Displays the providers required for the configuration.  
   - Example:  
     ```bash
     terraform providers
     ```

### **16. `terraform login`**
- Authenticates Terraform with Terraform Cloud or Enterprise.
- Example:
  ```bash
  terraform login
  ```

---

### **17. `terraform logout`**
- Logs out from Terraform Cloud or Enterprise.
- Example:
  ```bash
  terraform logout
  ```

---

### **18. `terraform refresh` (Deprecated)**
- Used to update the state file with the latest infrastructure changes **without applying them**.
- Replaced by `terraform apply -refresh-only`.
- Example:
  ```bash
  terraform refresh
  ```
  or
  ```bash
  terraform apply -refresh-only
  ```

---

### **19. `terraform force-unlock`**
- Unlocks the Terraform state file if a previous operation was interrupted.
- Useful when Terraform gets stuck in a locked state.
- Example:
  ```bash
  terraform force-unlock <LOCK_ID>
  ```

---

### **20. `terraform debug`**
- Enables debugging mode to troubleshoot Terraform issues.
- Example:
  ```bash
  TF_LOG=DEBUG terraform apply
  ```

---

### **21. `terraform test` (Experimental)**
- Runs unit tests on Terraform modules (introduced in Terraform 1.6).
- Example:
  ```bash
  terraform test
  ```

---

### **22. `terraform providers lock`**
- Locks Terraform provider versions.
- Example:
  ```bash
  terraform providers lock
  ```

---

### **23. `terraform providers mirror`**
- Creates a local mirror of provider plugins.
- Useful for air-gapped environments.
- Example:
  ```bash
  terraform providers mirror /path/to/local/directory
  ```

---

### **24. `terraform state replace-provider`**
- Replaces provider references in the Terraform state.
- Example:
  ```bash
  terraform state replace-provider 'old-provider' 'new-provider'
  ```

---

### **25. `terraform state mv`**
- Moves a resource within the state file.
- Example:
  ```bash
  terraform state mv old_resource_name new_resource_name
  ```

---

### **26. `terraform state pull`**
- Retrieves the current state file from remote storage.
- Example:
  ```bash
  terraform state pull > state.tfstate
  ```

---

### **27. `terraform state push`**
- Pushes a modified state file back to remote storage.
- Example:
  ```bash
  terraform state push state.tfstate
  ```

---

### **28. `terraform output -json`**
- Outputs Terraform values in JSON format.
- Example:
  ```bash
  terraform output -json
  ```

---

### **29. `terraform show -json`**
- Displays the Terraform state or plan file in JSON format.
- Example:
  ```bash
  terraform show -json tfplan
  ```

---

### **30. `terraform workspace delete`**
- Deletes a Terraform workspace.
- Example:
  ```bash
  terraform workspace delete dev
  ```

---

### **31. `terraform workspace list`**
- Lists all available workspaces.
- Example:
  ```bash
  terraform workspace list
  ```

---

### **32. `terraform workspace select`**
- Switches between different Terraform workspaces.
- Example:
  ```bash
  terraform workspace select staging
  ```

---

### **33. `terraform init -upgrade`**
- Upgrades installed provider plugins to the latest compatible versions.
- Example:
  ```bash
  terraform init -upgrade
  ```

---

### **34. `terraform plan -destroy`**
- Shows what will be destroyed before running `terraform destroy`.
- Example:
  ```bash
  terraform plan -destroy
  ```

---

### **35. `terraform apply -auto-approve`**
- Applies changes without asking for confirmation.
- Example:
  ```bash
  terraform apply -auto-approve
  ```

---

### **36. `terraform import -allow-missing-config`**
- Imports resources into Terraform state without requiring a corresponding `.tf` configuration.
- Example:
  ```bash
  terraform import -allow-missing-config aws_instance.example i-1234567890abcdef0
  ```

---

### **37. `terraform force-unlock -force <LOCK_ID>`**
- Forces unlocking of the Terraform state when necessary.
- Example:
  ```bash
  terraform force-unlock -force 1234567890
  ```

---

### **38. `terraform console`**
- Opens an interactive console to evaluate Terraform expressions.
- Example:
  ```bash
  terraform console
  ```
  Then, you can run:
  ```terraform
  length([1, 2, 3])
  ```

---

### **39. `terraform providers schema`**
- Displays the schema of providers used in the configuration.
- Example:
  ```bash
  terraform providers schema
  ```

---

### **40. `terraform graph | dot -Tsvg > graph.svg`**
- Generates a dependency graph in SVG format for visualization.
- Example:
  ```bash
  terraform graph | dot -Tsvg > graph.svg
  ```

---

