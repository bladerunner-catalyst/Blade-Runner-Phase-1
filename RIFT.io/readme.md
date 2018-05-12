This directory contains the following:

* API_Payloads – Capture of TM Forum Open APIs used by the SO
* Base - base service descriptors (NS and VNF Packages) containing NSD and VNFD
* Service Assurance – service descriptors with service assurance attributes added

All NS and VNF packages in the Base and Service Assurance directories are in TOSCA CSAR format according to ETSI NFV SOL 004.  The YAML descriptors (NSD and VNFD) are contained in the "Definitions" directory.

The Central Base NSD and Central Monitoring NSD contains a nested NSD that references the Local Base and Local Monitoring NSDs to be instantiated by du.

Contents:

NS

- Central Base
- Central Service Monitoring
- Local Base
- Local Service Monitoring

VNF

- Fortigate Firewall
- EXFO vVerifier vProbe
- Infosys ARVR
- Infosys VR Backend

Only the Fortigate vFIrewall VNF was modified with Service Assurance attributes.