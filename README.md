# SAP-Nuclei-Templates
Nuclei Templates for SAP Pentesting

## Collection

This collection contains already existing Nuclei templates for SAP as well as newly developed ones by me. The new ones are heavily inspired by already existing Metasploit SAP SOAP modules but ported to the Nuclei templates engine for ease of use. These new templates await approval by Nuclei to be added to the official Nuclei Template collection. Status [here](https://github.com/projectdiscovery/nuclei-templates/pull/14224).

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
  - sap-visual-composer-metadatauploader-detect.yaml

## Usage

> [!TIP]
> Conduct an Nmap TCP full port scan first to craft your `targets.txt`. Only provide root URLs with no paths.
>
> I highly recommend converting Nmap's XML into an HTML report using [nmap-bootstrap-xsl](https://github.com/Haxxnet/nmap-bootstrap-xsl). Provides super visibility and many features ([demo](https://haxxnet.github.io/nmap-bootstrap-xsl/report.html)). Leave a star if you like it!

```bash
# clone repo
git clone https://github.com/l4rm4nd/SAP-Nuclei-Templates

# run all sap nuclei templates
nuclei -l targets.txt -t ./SAP-Nuclei-Templates

# detect panels and basic info only
nuclei -l targets.txt -t ./SAP-Nuclei-Templates -s info

# run my custom sap templates only
nuclei -l targets.txt -t ./SAP-Nuclei-Templates -a LRVT
```
