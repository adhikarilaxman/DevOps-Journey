# DevOps Basics – My Learning Journey

This repository contains my notes and understanding of **DevOps concepts**.

---

## Day 11 Notes

### Shell Scripting Project Used in Real Time

**Goal:** To find out who has access to your GitHub repositories using a shell script.

---

### Shell Script

```bash
#!/bin/bash

# GitHub API URL
API_URL="https://api.github.com"

# GitHub username and personal access token (set these using export)
USERNAME=$username
TOKEN=$token

# Repository details (passed as arguments)
REPO_OWNER=$1
REPO_NAME=$2

# Function to call GitHub API
function github_api_get {
    local endpoint="$1"
    local url="${API_URL}/${endpoint}"
    curl -s -u "${USERNAME}:${TOKEN}" "$url"
}

# Function to list users with read access
function list_users_with_read_access {
    local endpoint="repos/${REPO_OWNER}/${REPO_NAME}/collaborators"

    # Get collaborators and filter those with read (pull) permission
    collaborators="$(github_api_get "$endpoint" | jq -r '.[] | select(.permissions.pull == true) | .login')"

    # Display result
    if [[ -z "$collaborators" ]]; then
        echo "No users with read access found for ${REPO_OWNER}/${REPO_NAME}."
    else
        echo "Users with read access to ${REPO_OWNER}/${REPO_NAME}:"
        echo "$collaborators"
    fi
}

# Main script execution
echo "Listing users with read access to ${REPO_OWNER}/${REPO_NAME}..."
list_users_with_read_access
```

---

### Steps to Run

1. **Launch an EC2 instance** (or any Linux machine).
2. **Create a file** using `vim` (e.g., `vim github-access.sh`).
3. **Paste the script** into the file and save it.
4. **Set your GitHub username**:

   ```bash
   export username="your-username"
   ```
5. **Set your GitHub API token**:

   ```bash
   export token="your-token"
   ```
6. **Install `jq`** for JSON parsing:

   ```bash
   sudo apt install jq -y
   ```
7. **Run the script** with repository details:

   ```bash
   ./github-access.sh <organisation-name> <repository-name>
   ```
8. ✅ You will see the list of users who have access to that repository.

---

### Screenshots

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/b894e6851db2394152204369c39550d288be9843/Day11/Day11%2001.png)

![image alt](https://github.com/adhikarilaxman/DevOps-Journey/blob/b894e6851db2394152204369c39550d288be9843/Day11/Day11%2002.png)

---
