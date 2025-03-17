# Upload Log Files to Splunk

## Step 1: Log in to Splunk
1. Open the Splunk web interface.
2. Enter your credentials and log in.
![image](https://github.com/user-attachments/assets/48dfd218-3662-4c05-9869-c2b7800e1d69)

## Step 2: Navigate to Data Upload
1. Go to **Settings** > **Add Data**.
2. Select **Upload** as the data input method.
![image](https://github.com/user-attachments/assets/33f7c7f7-5531-495a-838a-4e5bd2805201)

## Step 3: Choose File
1. Click on **Select File**.
2. Choose the sample DNS log file you prepared earlier.
![image](https://github.com/user-attachments/assets/c192cb14-bc80-4505-93bd-3cd1de115f94)

## Step 4: Set Source Type
1. In the **Set Source Type** section, specify the source type for the uploaded log file.
2. Choose the appropriate source type for DNS logs (e.g., `dns` or a custom source type if applicable).
![image](https://github.com/user-attachments/assets/2e737fe2-ce70-454e-9e33-e898d4c68d6b)

## Step 5: Review Settings
1. Check settings such as **index**, **host**, and **sourcetype**.
2. Ensure all settings match the sample DNS log file correctly.
![image](https://github.com/user-attachments/assets/55cf35ee-9444-47c8-8c23-9a4e1d65117d)

## Step 6: Upload the File
1. Click on the **Review** button.
2. Double-check the settings for accuracy.
3. Click **Submit** to upload the DNS log file to Splunk.
![image](https://github.com/user-attachments/assets/94d731f0-ab07-4603-9d17-4271ec1c87a6)

## Step 7: Verify Upload
1. After uploading, go to the **Search & Reporting** app.
2. Run a search query to verify that the uploaded DNS events are visible:
   ```spl
   index=<your_dns_index> sourcetype=<your_dns_sourcetype>
   ```
![image](https://github.com/user-attachments/assets/dbd33b0d-5220-407c-b2ea-9d9436f9c476)
