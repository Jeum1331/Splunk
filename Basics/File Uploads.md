# Upload Log Files to Splunk

## Step 1: Log in to Splunk
1. Open the Splunk web interface.
2. Enter your credentials and log in.

## Step 2: Navigate to Data Upload
1. Go to **Settings** > **Add Data**.
2. Select **Upload** as the data input method.

## Step 3: Choose File
1. Click on **Select File**.
2. Choose the sample DNS log file you prepared earlier.

## Step 4: Set Source Type
1. In the **Set Source Type** section, specify the source type for the uploaded log file.
2. Choose the appropriate source type for DNS logs (e.g., `dns` or a custom source type if applicable).

## Step 5: Review Settings
1. Check settings such as **index**, **host**, and **sourcetype**.
2. Ensure all settings match the sample DNS log file correctly.

## Step 6: Upload the File
1. Click on the **Review** button.
2. Double-check the settings for accuracy.
3. Click **Submit** to upload the DNS log file to Splunk.

## Step 7: Verify Upload
1. After uploading, go to the **Search & Reporting** app.
2. Run a search query to verify that the uploaded DNS events are visible:
   ```spl
   index=<your_dns_index> sourcetype=<your_dns_sourcetype>
   ```
