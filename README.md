## Installation

### 1. Install the package

Install the apt-repo-sixfab package.

```bash
wget https://github.com/sixfab/sixfab_dx/releases/download/v0.1/apt-repo-sixfab.deb
sudo dpkg -i apt-repo-sixfab.deb
```

### 2. Install sixfab-dx package

```bash
sudo apt update && sudo apt install sixfab-dx
```

### 3. Enable PCIe Gen 3 for optimal performance

To get the best inference throughput from the DX-M1 NPU, open the boot configuration file:

```bash
sudo nano /boot/firmware/config.txt
```

Add the following lines at the end of the file:

```bash
dtparam=pciex1
dtparam=pciex1_gen=3
```

Save and exit (Ctrl+X, then Y, then Enter), then reboot:

```bash
sudo reboot
```

## Confirmation

```bash
dxrt-cli -s
```

## Updating

Use the standard APT workflow to update to newer versions:

```bash
sudo apt update && sudo apt upgrade sixfab-dx
```

## Uninstallation

To remove the package and clean up the repository configuration:

```bash
sudo apt remove sixfab-dx sixfab-dx-onnxruntime dxrt-driver-dkms
```

## Support

For any help, visit [Sixfab Support](https://sixfab.com/contact/).
