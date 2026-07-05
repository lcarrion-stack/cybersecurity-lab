# Finding 001 - Windows Server Service Exposure

## Asset
Windows Server (192.168.100.10)

## Tool Used
nmap -sV -O

## Evidence
File: scans/nmap/windows-server-services.txt

## Observations
- Open ports discovered from scan output
- Services and versions identified via service detection (-sV)
- Operating system fingerprint suggests Windows Server environment

## Risk Rating
Medium (depends on exposed services)

## Security Impact
Exposed services may provide attack surface for:
- Credential attacks
- Service exploitation
- Misconfiguration abuse

## Recommendation
- Restrict unnecessary ports using firewall rules in OPNsense
- Disable unused services
- Limit SMB/WinRM exposure to trusted VLAN only
- Enable logging and monitoring on all exposed services
