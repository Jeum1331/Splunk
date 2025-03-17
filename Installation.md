<!DOCTYPE html>
<html>
<head>
    <title>Installing Splunk on Windows</title>
    <meta charset="UTF-8">
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
        }
        h1, h2 {
            color: #005a9c;
        }
        code {
            background-color: #f4f4f4;
            padding: 2px 5px;
            border-radius: 4px;
        }
        pre {
            background: #eee;
            padding: 10px;
            border-radius: 5px;
            overflow-x: auto;
        }
    </style>
</head>
<body>
    <h1>Installing Splunk on Windows</h1>
    <p>This guide walks you through the installation of Splunk on a Windows computer.</p>
    
    <h2>Step 1: Download Splunk</h2>
    <ol>
        <li>Visit the <a href="https://www.splunk.com/en_us/download.html" target="_blank">Splunk Download Page</a>.</li>
        <li>Sign in or create an account if required.</li>
        <li>Download the Windows Installer (typically a <code>.msi</code> file).</li>
    </ol>
    
    <h2>Step 2: Install Splunk</h2>
    <ol>
        <li>Locate the downloaded <code>.msi</code> file and double-click to run it.</li>
        <li>Follow the installation wizard:</li>
        <ul>
            <li>Accept the license agreement.</li>
            <li>Choose an installation directory (default is <code>C:\Program Files\Splunk</code>).</li>
            <li>Set up an administrator username and password.</li>
        </ul>
        <li>Click <strong>Install</strong> and wait for the installation to complete.</li>
    </ol>
    
    <h2>Step 3: Start Splunk</h2>
    <ol>
        <li>Open the Command Prompt as Administrator.</li>
        <li>Navigate to the Splunk bin directory:</li>
        <pre>cd "C:\Program Files\Splunk\bin"</pre>
        <li>Start Splunk:</li>
        <pre>splunk start</pre>
        <li>If prompted, accept the Splunk license agreement.</li>
    </ol>
    
    <h2>Step 4: Access Splunk Web Interface</h2>
    <ol>
        <li>Open a web browser and go to: <a href="http://localhost:8000" target="_blank">http://localhost:8000</a></li>
        <li>Log in with the administrator credentials you set during installation.</li>
    </ol>
    
    <h2>Troubleshooting</h2>
    <ul>
        <li>If Splunk does not start, check the logs in <code>C:\Program Files\Splunk\var\log\splunk</code>.</li>
        <li>Ensure port 8000 is not blocked by your firewall.</li>
        <li>Run Splunk as Administrator for proper permissions.</li>
    </ul>
    
    <h2>Uninstalling Splunk</h2>
    <ol>
        <li>Stop Splunk from the Command Prompt:</li>
        <pre>splunk stop</pre>
        <li>Go to Control Panel &gt; Programs &gt; Uninstall a Program.</li>
        <li>Find Splunk in the list and click <strong>Uninstall</strong>.</li>
    </ol>
    
    <p><strong>Congratulations! 🎉 You have successfully installed Splunk on Windows.</strong></p>
</body>
</html>
    
