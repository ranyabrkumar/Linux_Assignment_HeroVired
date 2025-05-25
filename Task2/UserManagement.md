# User Management

## 2. User Management & Access Control

- Create user accounts for new developers (e.g., Sarah and Mike)
- Assign each user an isolated workspace directory
- Set directory permissions so only the owner can access
- Enforce password expiration and complexity

### Commands:

```bash

# Create users
sudo useradd -m -d /Sarah sarah
sudo useradd -m -d /mike mike
sudo passwd sarah
sudo passwd mike

# Create and secure workspaces
sudo mkdir -p /Sarah/workspace /mike/workspace
sudo chown sarah:sarah /Sarah/workspace
sudo chown mike:mike /mike/workspace
sudo chmod 700 /Sarah/workspace /mike/workspace

# Set password expiration
sudo chage -M 30 sarah
sudo chage -M 30 mike
```

---

