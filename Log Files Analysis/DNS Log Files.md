# Steps to Analyze DNS Log Files

## Step 1: Search for DNS Events
1. Open the Splunk interface and navigate to the search bar.
2. Use the following query to retrieve DNS events:
   ```spl
   index=* sourcetype=dns
   ```
![image](https://github.com/user-attachments/assets/d88e6009-7c34-4413-948c-fc244eea2287)

## Step 2: Extract Key Fields
1. Identify important fields in DNS logs such as:
_time: The timestamp of the event.
fqdn: Fully Qualified Domain Name.
query: The DNS query that was made.
host: The source host of the DNS request.
source: The file or log source.
sourcetype: The type of the event (dns in this case).
And so on.
When to Use:
This is useful when you want to inspect the raw data in a tabular form and check out all fields, especially if you’re not sure which fields exist in your DNS data.
It helps you explore your DNS data and identify important fields that you can later filter, group, or analyze.
![image](https://github.com/user-attachments/assets/4d000154-ee00-4839-9dc9-dbf6e800b85d)

3. Apply a regex filter to extract relevant DNS-related data:
   ```spl
   index=* sourcetype=dns_sample | regex _raw="(?i)\b(dns|domain|query|response|port 53)\b"
   ```

## Step 3: Detect Anomalous Activity
1. Look for unusual trends or irregularities in DNS traffic.
2. Use the following query to detect spikes in DNS requests:
   ```spl
   index=_* OR index=* sourcetype=dns | table *
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
