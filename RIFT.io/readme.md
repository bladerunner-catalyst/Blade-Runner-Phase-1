This directory contains four ETSI Network Service Packages and their constituent
VNF Packages.

The Base directory contains the base descriptors without the Service Assurance 
extensions.  The Service Assurance directory has the base descriptors with the 
SA attributes added.

All packages are in TOSCA CSAR format according to ETSI NFV SOL 004.  The
YAML descriptors (NSD and VNFD) are contained in the "Definitions" directory.

The Central Base NSD and Central Monitoring NSD contains a nested NSD that
references the Local Base and Local Monitoring NSDs to be instantiated by du.

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
