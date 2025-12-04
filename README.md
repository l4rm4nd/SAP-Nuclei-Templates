# SAP-Nuclei-Templates
Nuclei Templates for SAP Pentesting

## Collection

This collection contains already existing Nuclei templates for SAP as well as newly developed ones by me. The new ones are heavily based on already existing Metasploit SAP SOAP modules but ported as Nuclei templates for ease of use. These new templates await approval by Nuclei to be added to the official Nuclei Template collection. Status [here](https://github.com/projectdiscovery/nuclei-templates/pull/14224).

- Existing templates collected from official Nuclei Templates:
  - http/technologies/sap
  - nuclei-templates/http/misconfiguration/sap

- New ones developed by me or ported from Metasploit:
  - sap-management-console-panel.yaml
  - sap-message-server-console-exposed.yaml
  - sap-message-server-detect.yaml
  - sap-sapcontrol-abapreadsyslog-log-disclosure.yaml
  - sap-sapcontrol-getenvironment-env-disclosure.yaml
  - sap-sapcontrol-getinstanceproperties.yaml
  - sap-sapcontrol-getversioninfo.yaml
  - sap-sapcontrol-listconfigfiles-config-enum.yaml
  - sap-sapcontrol-listlogfiles-log-enum.yaml
  - sap-sapcontrol-osexecute-unauth-rce.yaml
  - sap-sapcontrol-readconfigfile-config-disclosure.yaml
  - sap-sapcontrol-readlogfile-log_disclosure.yaml

## Usage

```bash
# clone repo
git clone https://github.com/l4rm4nd/SAP-Nuclei-Templates

# run nuclei
nuclei -l targets.txt -t ./SAP-Nuclei-Templates
```
