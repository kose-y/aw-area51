# User Guide

## System information

* Chassis: Alienware Area51 R5. Full specs <https://www.dell.com/support/manuals/us/en/04/alienware-area51-r4/alienwarearea51r5_setupandspecs/specifications?guid=guid-2795f926-e3d3-4d85-9813-11a63248dabb&lang=en-us>

* CPU: Intel i9 9920X (12 core, 12.288MB L2 Cache, 19.712MB L3 Cache, 3.5 GHz up to 4.5GHz with Intel Turbo Boost Max 3.0). Full specs: <https://ark.intel.com/content/www/us/en/ark/products/189127/intel-core-i9-9920x-x-series-processor-19-25m-cache-up-to-4-50-ghz.html>.

* GPU: NVIDIA GeForce RTX 2080 Ti OC with 11GB GDDR6 (14 Gbps), 4352 cores, SP 13.4 TFLOPs, INT4 430TOPs. Full specs <https://www.nvidia.com/en-us/geforce/graphics-cards/rtx-2080-ti/>.

* Memory: 64GB DDR4 SDRAM, 4 slots of 16GB, 2666 MHz.

* SSD 1 (Kingston): 512GB PCIe NVMe M.2 SSD, CentOS 7 bootable.

* SSD 2 (Kodak): 920GB SATA III SSD, mounted on `/mnt/AppRun`. Use this as scratch for big data computing (ephemeral).


* Hard drive 1 (WD Black Performance SATA): 6TB, formatted as EXT4, mounted at `/mnt/Data1`. Use this for large, permanent data sets.


* Hard drive 2 (WD Black Performance SATA): 6TB, formatted as EXT4, mounted at `/mnt/Data2`. Use this for large, permanent data sets.


* IPv4: 10.47.201.62 (eth2, 1000 Mbps).


* USB flash drives: will be mounted at `/run/media/[USERNAME]/[DRIVENAME]`, e.g., `/run/media/huazhou/SanDisk64GB`.


* Operating system: CentOS 7.


* Available Editors: vi, vim, emacs, nano, code (VS Code).

## How to establish an account?

Email Dr. Hua Zhou <huazhou@ucla.edu>. Upon approval, you'll receive an email with username and one-time password.  Log in and change passwood IMMEDIATELY, using Linux command `passwd`.

## Connection to the machine

- Prerequisites for connecting to the machine: 

	- If you are in CHS building and connected via ethernet cable, then `ssh 10.47.201.62` should work.

	- If you want to use WIFI (NOT WORKING YET), then:
		1. You need a UCLA MedNet account. 
		2. On campus, you have to use the `UCLAHealthSecure` wifi. 
		3. Off campus, you have to use the GobalProtect VPN Client and OnGuard associated with your MedNet acccount. See
<https://mednet.uclahealth.org/device-security-toolkit/> for instructions. You need to file an IT service request at <https://mednet.uclahealth.org/it-service-catalog-quick-links/> to allow you use VPN over MedNet.

- How to connect to AW Area51?
`ssh <YourUserName>@10.47.201.62`
Using SSH keys is highly recommended. 

## R and RStudio

RStudio Server can be accessed at <10.47.201.62:8787>.
R version is v3.5.0. Many commonly used R packages (tidyverse, shiny, etc) are already installed systemwide and available to all users. You can find installed packages by R command `installed.packages()`. You can install extra packages, which will be put in your home directory (`~/R` by default).

## Julia

Julia v1.1.1 is available. Since v1.0, all Julia packages will be installed in user home directories.


## Jupyter

- JupyterHub can be accessed at <10.47.201.62:8000>

- Available Jupyter Notebook kernels: R, Python 2, Python 3, Julia 1.1.1, bash.

## VS Code

You can also use VS Code on your local machine (laptop or desktop) to develop code on the server. 

1. Make sure SSH key connection with the server works.

2. Install the `Remote Development extension pack` in VS Code.

3. In VS Code, Run `Remote-SSH: Connect to Host...` from the Command Palette (`F1`) and enter `user@hostname`.

Read <https://code.visualstudio.com/docs/remote/ssh> for details.
