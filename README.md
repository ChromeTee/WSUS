# WSUS
## Windows Server Update Services

– Caches Microsoft Updates for devices within the enclave
• Saves bandwidth

– Provides Centralized Management of Updates with Active  Directory
• Only allow approved updates
• Force updates for client workstations
• Allows for grouping of like devices with separate policies
• Auditing of currently unapproved patches

– WSUS is flexible in timing when updates are applied
• Set time for each client to check for WSUS updates
• Allows administrators to set after hours updates to minimize bandwidth impact.

– Generates reports based on current update status of managed devices

– No additional license requirements
• Free with Windows Server XXXX

### Windows Update Agent connects to WSUS via HTTP/HTTPS, checks for update:
– WSUS Version 3.2 and earlier: TCP 80, 443
– WSUS 6.2 (Server 2012) and later: TCP 8530, 8531

### WSUS Server Responds and provides updates
– Based on Update Groups

### Installation options WSUS Server:

– Internet Connected
• Select “Add A Role” in Server Manager
• Point to Microsoft or Upstream Server for Updates

– Offline

• Airgap Required Binaries to Server
– https://www.microsoft.com/en-us/download/details.aspx?id=5216

• Point to Upstream Server for Updates or Create WSUS Export Server
– https://blogs.msdn.microsoft.com/george_bethanis/2014/09/19/how-toinstall-patches-in-an-isolated-environment/

• Using Group Policy to enforce Client Update Settings
– GPMC > Computer Configuration>Policies > Administrative Templates > Windows Components > Windows Update > Specify Intranet Microsoft Update Service Location
– GPMC > Computer Configuration>Policies > Administrative Templates > Windows Components>Windows Update > Configure Automatic Updates

• Automatically assign assets to a WSUS group based on Group Policy
– GPMC > Computer Configuration>Policies > Administrative Templates > Windows Components>Windows Update>Enable client-side targeting

