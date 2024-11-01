# tftp-server-al2023-for-l1-tftpboot
tftp-server-al2023-for-l1-tftpboot

# usage
```
[ec2-user@ip-172-31-240-179 ~]$ wget https://github.com/sigitp-git/tftp-server-al2023-for-l1-tftpboot/raw/refs/heads/main/scratch-tftp.zip
--2024-10-31 17:26:14--  https://github.com/sigitp-git/tftp-server-al2023-for-l1-tftpboot/raw/refs/heads/main/scratch-tftp.zip
Resolving github.com (github.com)... 140.82.116.4
Connecting to github.com (github.com)|140.82.116.4|:443... connected.
HTTP request sent, awaiting response... 302 Found
Location: https://raw.githubusercontent.com/sigitp-git/tftp-server-al2023-for-l1-tftpboot/refs/heads/main/scratch-tftp.zip [following]
--2024-10-31 17:26:15--  https://raw.githubusercontent.com/sigitp-git/tftp-server-al2023-for-l1-tftpboot/refs/heads/main/scratch-tftp.zip
Resolving raw.githubusercontent.com (raw.githubusercontent.com)... 185.199.110.133, 185.199.111.133, 185.199.108.133, ...
Connecting to raw.githubusercontent.com (raw.githubusercontent.com)|185.199.110.133|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 504043 (492K) [application/zip]
Saving to: ‘scratch-tftp.zip’

scratch-tftp.zip                                                    100%[=================================================================================================================================================================>] 492.23K  --.-KB/s    in 0.09s

2024-10-31 17:26:15 (5.52 MB/s) - ‘scratch-tftp.zip’ saved [504043/504043]

[ec2-user@ip-172-31-240-179 ~]$ unzip scratch-tftp.zip
Archive:  scratch-tftp.zip
   creating: scratch-tftp/
  inflating: scratch-tftp/tftp-5.2-43.amzn2023.x86_64.rpm
  inflating: scratch-tftp/tftp-5.2-43.amzn2023.src.rpm
  inflating: scratch-tftp/tftp-debugsource-5.2-43.amzn2023.x86_64.rpm
  inflating: scratch-tftp/tftp-debugsource-5.2-43.amzn2023.aarch64.rpm
  inflating: scratch-tftp/tftp-server-debuginfo-5.2-43.amzn2023.x86_64.rpm
  inflating: scratch-tftp/tftp-server-5.2-43.amzn2023.x86_64.rpm
  inflating: scratch-tftp/tftp-5.2-43.amzn2023.aarch64.rpm
  inflating: scratch-tftp/tftp-debuginfo-5.2-43.amzn2023.aarch64.rpm
  inflating: scratch-tftp/tftp-debuginfo-5.2-43.amzn2023.x86_64.rpm
  inflating: scratch-tftp/tftp-server-debuginfo-5.2-43.amzn2023.aarch64.rpm
  inflating: scratch-tftp/tftp-server-5.2-43.amzn2023.aarch64.rpm
[ec2-user@ip-172-31-240-179 ~]$

[ec2-user@ip-172-31-240-179 scratch-tftp]$ sudo yum localinstall tftp-server-5.2-43.amzn2023.aarch64.rpm
Amazon Linux 2023 repository                                                                                                                                                                                                                  0.0  B/s |   0  B     00:00
Errors during downloading metadata for repository 'amazonlinux':
  - Curl error (6): Couldn't resolve host name for https://al2023-repos-default-de612dc2.s3.dualstack.default.amazonaws.com/core/mirrors/2023.4.20240416/aarch64/mirror.list [Could not resolve host: al2023-repos-default-de612dc2.s3.dualstack.default.amazonaws.com]
Error: Failed to download metadata for repo 'amazonlinux': Cannot prepare internal mirrorlist: Curl error (6): Couldn't resolve host name for https://al2023-repos-default-de612dc2.s3.dualstack.default.amazonaws.com/core/mirrors/2023.4.20240416/aarch64/mirror.list [Could not resolve host: al2023-repos-default-de612dc2.s3.dualstack.default.amazonaws.com]
Amazon Linux 2023 Kernel Livepatch repository                                                                                                                                                                                                 0.0  B/s |   0  B     00:00
Errors during downloading metadata for repository 'kernel-livepatch':
  - Curl error (6): Couldn't resolve host name for https://al2023-repos-default-de612dc2.s3.dualstack.default.amazonaws.com/kernel-livepatch/mirrors/al2023/aarch64/mirror.list [Could not resolve host: al2023-repos-default-de612dc2.s3.dualstack.default.amazonaws.com]
Error: Failed to download metadata for repo 'kernel-livepatch': Cannot prepare internal mirrorlist: Curl error (6): Couldn't resolve host name for https://al2023-repos-default-de612dc2.s3.dualstack.default.amazonaws.com/kernel-livepatch/mirrors/al2023/aarch64/mirror.list [Could not resolve host: al2023-repos-default-de612dc2.s3.dualstack.default.amazonaws.com]
Ignoring repositories: amazonlinux, kernel-livepatch
Dependencies resolved.
==============================================================================================================================================================================================================================================================================
 Package                                                          Architecture                                                 Version                                                                Repository                                                         Size
==============================================================================================================================================================================================================================================================================
Installing:
 tftp-server                                                      aarch64                                                      5.2-43.amzn2023                                                        @commandline                                                       40 k

Transaction Summary
==============================================================================================================================================================================================================================================================================
Install  1 Package

Total size: 40 k
Installed size: 216 k
Is this ok [y/N]: y
Downloading Packages:
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Running transaction
  Preparing        :                                                                                                                                                                                                                                                      1/1
  Installing       : tftp-server-5.2-43.amzn2023.aarch64                                                                                                                                                                                                                  1/1
  Running scriptlet: tftp-server-5.2-43.amzn2023.aarch64                                                                                                                                                                                                                  1/1
  Verifying        : tftp-server-5.2-43.amzn2023.aarch64                                                                                                                                                                                                                  1/1
Error encountered while trying to retrieve release update information: Unable to retrieve release info data. Curl error (6): Couldn't resolve host name for https://al2023-repos-default-de612dc2.s3.dualstack.default.amazonaws.com/core/releasemd.xml [Could not resolve host: al2023-repos-default-de612dc2.s3.dualstack.default.amazonaws.com]

Installed:
  tftp-server-5.2-43.amzn2023.aarch64

Complete!
```
