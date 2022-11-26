# 5G-AiaB-without-ROC

Deploying Aether's 5G SD-CORE without ROC using Helm Charts. [Official Documentation](https://docs.sd-core.opennetworking.org/master/developer/aiab5g.html)

## Pre-requisite

* Ubuntu 18.04 or higher stable version (18.04 is a requirement of OAISIM which is used to test 4G Aether).

* Kernel 4.15 or later.

* Haswell CPU or newer.

* Install `make`:

```bash
sudo apt install -y make
```

## Installation

### Clone Repositories

```bash
git clone "https://gerrit.opencord.org/aether-in-a-box"
mkdir cord
cd cord/
git clone "https://gerrit.opencord.org/sdcore-helm-charts"
```

### Deploy 5G SD-CORE

```bash
cd ..
cd aether-in-a-box/
make 5g-core
```

To deploy and test 5G SD-CORE:

```bash
make 5g-test
```

### Check Pods

```bash
kubectl get pods -A
```

![image](https://user-images.githubusercontent.com/97805339/204111906-a67f1f20-5342-437d-86a6-851265e9fdca.png)

