# Steps to Analyze DNS Log Files

## Step 1: Search for DNS Events
1. Open the Splunk interface and navigate to the search bar.
2. Use the following query to retrieve DNS events:
   ```spl
   index=* sourcetype=dns_sample
   ```
![image](https://github.com/user-attachments/assets/d88e6009-7c34-4413-948c-fc244eea2287)

## Step 2: Extract Key Fields
1. Identify important fields in DNS logs such as:
   - Source IP
   - Destination IP
   - Domain Name
   - Query Type
   - Response Code
2. Apply a regex filter to extract relevant DNS-related data:
   ```spl
   index=* sourcetype=dns_sample | regex _raw="(?i)\b(dns|domain|query|response|port 53)\b"
   ```

## Step 3: Detect Anomalous Activity
1. Look for unusual trends or irregularities in DNS traffic.
2. Use the following query to detect spikes in DNS requests:
   ```spl
   index=_* OR index=* sourcetype=dns_sample | stats count by fqdn
   ```

## Step 4: Identify Top DNS Sources
1. Use the `top` command to list the most frequently queried domains and their source IPs:
   ```spl
   index=* sourcetype=dns_sample | top fqdn, src_ip
   ```

## Step 5: Investigate Potential Threats
1. Search for domains linked to suspicious or malicious activity.
2. Utilize threat intelligence services or domain reputation databases like [VirusTotal](https://www.virustotal.com).
3. Example query to check for known malicious domains:
   ```spl
   index=* sourcetype=dns_sample fqdn="maliciousdomain.com"
   ```

## Conclusion
Utilizing Splunk for DNS log analysis empowers security professionals to detect threats and respond to incidents more effectively. By monitoring DNS activity and identifying anomalies, organizations can strengthen their security defenses and mitigate cyber risks.
