# Installing Splunk on Windows

## Introduction
This guide provides step-by-step instructions for installing Splunk on a Windows computer.

## Step 1: Download Splunk
1. Visit the [Splunk Download Page](https://www.splunk.com/en_us/download.html).
2. Sign in or create an account if required.
3. Download the Windows Installer (typically a `.msi` file).
![image](https://github.com/user-attachments/assets/f1a0173e-2236-4ebb-8c50-5358fc524aec)

## Step 2: Install Splunk
1. Locate the downloaded `.msi` file and double-click to run it.
2. Follow the installation wizard:
   - Accept the license agreement.
   - Choose an installation directory (default is `C:\Program Files\Splunk`).
   - Set up an administrator username and password.
3. Click **Install** and wait for the installation to complete.
![image](https://github.com/user-attachments/assets/52f50526-a59d-4574-a2b6-53804fea2767)

## Step 3: Start Splunk
1. Open the Command Prompt as Administrator.
2. Navigate to the Splunk bin directory:
   ```sh
   cd "C:\Program Files\Splunk\bin"
   ```
3. Start Splunk:
   ```sh
   splunk start
   ```
4. If prompted, accept the Splunk license agreement.

## Step 4: Access Splunk Web Interface
1. Open a web browser and go to: [http://localhost:8000](http://localhost:8000)
2. Log in with the administrator credentials you set during installation.
![image](https://github.com/user-attachments/assets/db47cdbe-8a09-4f84-9fbc-0013063d735e)
