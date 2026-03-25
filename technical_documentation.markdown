# Digital Research Alliance of Canada (the Alliance)

## Systems
General-purpose clusters, for GPU or CPU jobs:<br>
- Fir -> Fir's compute nodes have full access to the internet.
- Nibi -> All nodes on Nibi have Internet access, no special firewall permission or proxying is necessary.
- Narval -> Narval's compute nodes cannot access the internet, exception may apply.
- Rorqual -> Rorqual's compute nodes cannot access the internet, exception may apply.

Trillium, a cluster designed for large parallel jobs.<br>

## Services
Available software -> <https://docs.alliancecan.ca/wiki/Available_software><br>
Cloud computing service -> <https://docs.alliancecan.ca/wiki/Cloud><br>
Database servers -> <https://docs.alliancecan.ca/wiki/Database_servers><br>
Globus file transfer service -> can be accessed via the main Globus website or via the Alliance Globus portal<br>
Nextcloud cloud storage service -> a Dropbox-like cloud storage service, for all Alliance users<br>
Research Data Management -> <https://www.alliancecan.ca/en/services/research-data-management><br>
Research Software -> CERN Virtual Machine File System (CVMFS), Jupyter Hub, Magic Castle, Software Repository.<br>
Quantum computing services -> MonarQ available via the Narval cluster.<br>

## Trillium quickstart
1. Via Browser with Open OnDemand
2. Terminal access with ssh
Use this command to log into one of the login nodes of the CPU subcluster:
```
$ ssh -i /PATH/TO/SSH_PRIVATE_KEY  MYALLIANCEUSERNAME@trillium.scinet.utoronto.ca
```
To log into the login node for the GPU cluster, use this command
```
$ ssh -i /PATH/TO/SSH_PRIVATE_KEY  MYALLIANCEUSERNAME@trillium-gpu.scinet.utoronto.ca
```
Note:<br>
The Trillium login nodes are where you develop, edit, compile, prepare and submit jobs.<br>
The CPU login nodes and the GPU login node are not part of the compute nodes but they have the same architecture, operating system, and software stack as the CPU and GPU compute nodes, respectively.<br>
You can ssh from one login node to another using their internal hostnames `tri-login01`, ..., `tri-login06` and `trig-login01` (the latter is the GPU login node).<br>
If you add the option -Y you enable X11 forwarding, which allows graphical programs on Trillium to open windows on your local computer.<br>
To run on compute nodes, you must submit a batch job.<br>


source: https://docs.alliancecan.ca/wiki/Technical_documentation
