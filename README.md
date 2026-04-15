## Installation

### 1. Add the GPG key

Download the public key and add it to your system to verify the repository's signature:

```bash
wget -qO - https://sixfab.github.io/sixfab_dx/public.gpg | sudo gpg --dearmor -o /usr/share/keyrings/sixfab-dx.gpg
```

### 2. Add the APT repository

Register the Sixfab DX repository in your APT sources:

```bash
echo "deb [signed-by=/usr/share/keyrings/sixfab-dx.gpg] https://sixfab.github.io/sixfab_dx trixie main" | sudo tee /etc/apt/sources.list.d/sixfab-dx.list
```

### 3. Install the package

Update the package list and install `sixfab-dx`:

```bash
sudo apt update && sudo apt install sixfab-dx
```

## Updating

Use the standard APT workflow to update to newer versions:

```bash
sudo apt update && sudo apt upgrade sixfab-dx
```

## Uninstallation

To remove the package and clean up the repository configuration:

```bash
sudo apt remove sixfab-dx
sudo rm /etc/apt/sources.list.d/sixfab-dx.list
sudo rm /usr/share/keyrings/sixfab-dx.gpg
sudo apt update
```

## Support

For any help, visit [Sixfab Support](https://sixfab.com/contact/).
