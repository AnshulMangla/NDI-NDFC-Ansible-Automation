# NDI-NDFC-Ansible-Automation
Using Nexus Dashboard Insights to drive Analyis and Compliance Automation on NDFC


## Run Delta Analysis between last two epochs

This Playbook:
* Runs Delta Analysis between last two epochs.

 > $: ansible-playbook -i ndi-sites.yml playbook-delta-analysis-ndfc-latest-epochs.yml

## Run Delta Analysis between pre deployment epoch and the epoch created for latest Instant Assurance Analysis

This Playbook:
* Runs an Instant Assurance Analysis and hence creates an Epoch
* Runs a Delta Analysis between the epoch before the change and the epoch created from the Assurance Analysis job which was run earlier.
  
 > $: ansible-playbook -i ndi-sites.yml playbook-instant-delta-analysis-validate-ndfc.yml

P.S. This Playbook assumes that the earlier epoch was created before the deployment of the change
