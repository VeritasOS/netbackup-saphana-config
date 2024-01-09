#netbackup-saphana-config

##Description

Veritas NetBackup SAP HANA Agent integrates the SAP HANA backint interface.
The SAP HANA backup and recovery management capabilities are provided by NetBackup. 
To protect SAP HANA following configurations are required.
    1. Create hdbbackint softlink from /usr/sap/<SID>/SYS/global/hdb/opt/hdbbackint to /usr/openv/NetBackup/bin/hdbbackint_script
    2. Create NetBackup policies with retention daily, weekly, monthly.
    3. Create the parameter files (utl)
    4. Configure the parameter files (utl) in SAP HANA environment for Instance and tenant-DB
    5. Configure parameter files (utl) for SAP HANA data, log and catalog backups. 
    6. Create the backup scripts for Instance and tenant-DB
 
##Assumptions
	1. To utilize this role, in-depth knowledge of both Veritas NetBackup and Ansible is required.
	2. All the NetBackup Primary/Media servers and Client (SAP HANA systems) should be accessible from the ansible host.

##How to use this project
	1. Clone the repository from GitHub and move to your Ansible Control Host:
		git clone http://www.GitHub/netbackup-saphana-config.git
	2. Modify the sample_playbook_netbackup_sap_hana_config.yml file according to the SAP HANA environment
	3. Run the following command to run the playbook
		# ansible-playbook playbook_netbackup_sap_hana_config.yml -i inventory/hosts.yml

# License

The following components are available under the General Public License "GPL" 2.0 and/or the General Public License "GPL 3.0" provided herein. The source code for these GPL component(s) may be obtained at: https://github.com/VeritasOS/netbackup-saphana-config

## Legal Notice
Last updated: 2021-07-23
Legal Notice
Copyright © 2021 Veritas Technologies LLC. All rights reserved.
Veritas, the Veritas Logo, and NetBackup are trademarks or registered trademarks of Veritas Technologies LLC or its affiliates in the U.S. and other countries. Other names may be trademarks of their respective owners.
This product may contain third-party software for which Veritas is required to provide attribution to the third party ("Third-party Programs"). Some of the Third-party Programs are available under open source or free software licenses. The License Agreement accompanying the Software does not alter any rights or obligations you may have under those open source or free software licenses. Refer to the Third-party Legal Notices document accompanying this Veritas product or available at: https://www.veritas.com/about/legal/license-agreements
The product described in this document is distributed under licenses restricting its use, copying, distribution, and decompilation/reverse engineering. No part of this document may be reproduced in any form by any means without prior written authorization of Veritas Technologies LLC and its licensors, if any.
THE DOCUMENTATION IS PROVIDED "AS IS" AND ALL EXPRESS OR IMPLIED CONDITIONS, REPRESENTATIONS AND WARRANTIES, INCLUDING ANY IMPLIED WARRANTY OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE OR NON-INFRINGEMENT, ARE DISCLAIMED, EXCEPT TO THE EXTENT THAT SUCH DISCLAIMERS ARE HELD TO BE LEGALLY INVALID. VERITAS TECHNOLOGIES LLC SHALL NOT BE LIABLE FOR INCIDENTAL OR CONSEQUENTIAL DAMAGES IN
CONNECTION WITH THE FURNISHING, PERFORMANCE, OR USE OF THIS
DOCUMENTATION. THE INFORMATION CONTAINED IN THIS DOCUMENTATION IS SUBJECT TO CHANGE WITHOUT NOTICE.

The Licensed Software and Documentation are deemed to be commercial computer software as defined in FAR 12.212 and subject to restricted rights as defined in FAR Section 52.227-19 "Commercial Computer Software - Restricted Rights" and DFARS 227.7202, et seq. "Commercial Computer Software and Commercial Computer Software Documentation," as applicable, and any successor regulations, whether delivered by Veritas as on premises or hosted services. Any use, modification, reproduction release, performance, display or disclosure
of the Licensed Software and Documentation by the U.S. Government shall be solely in accordance with the terms of this Agreement.
Veritas Technologies LLC
2625 Augustine Drive
Santa Clara, CA 95054
http://www.veritas.com

## Third-Party Legal Notices
This Veritas product may contain third party software for which Veritas is required to provide attribution ("Third Party Programs"). Some of the Third Party Programs are available under open source or free software licenses. The License Agreement accompanying the Licensed Software does not alter any rights or obligations you may have under those open source or free software licenses. This document or appendix contains proprietary notices for the Third Party Programs and the licenses for the Third Party Programs, where applicable.
The following copyright statements and licenses apply to various open source software components (or portions thereof) that are distributed with the Licensed Software.

