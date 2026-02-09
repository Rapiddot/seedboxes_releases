# Seedboxes APT Repository

## Adding the Repository

### Step 1: Add the GPG key

```bash
curl -fsSL https://releases.seedboxes.cc/apt/seedboxes-repo-key.gpg | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/seedboxes.gpg > /dev/null
```

### Step 2: Add the repository to sources

```bash
echo "deb [arch=amd64,arm64] https://releases.seedboxes.cc/apt stable main" | sudo tee /etc/apt/sources.list.d/seedboxes.list
```

### Step 3: Update and install

```bash
sudo apt update
sudo apt install sbagent
```

## Available Packages

- **sbagent** - Seedbucket Remote Agent (GUI application)

## Verifying the Repository

You can verify the repository signature:

```bash
apt-cache policy sbagent
```

## Removing the Repository

```bash
sudo rm /etc/apt/sources.list.d/seedboxes.list
sudo rm /etc/apt/trusted.gpg.d/seedboxes.gpg
sudo apt update
```

## Repository Information

- **Origin:** Seedboxes
- **Components:** main
- **Architectures:** amd64, arm64
- **Codename:** stable

## Support

For issues with packages in this repository, please visit:
https://github.com/Rapiddot/seedboxes_releases/issues
