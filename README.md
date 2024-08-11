# Email Automation Script

## Overview
This Python script automates the process of sending emails to multiple recipients with optional file attachments and embedded images. It is designed for ease of use, allowing users to send personalized emails to a list of companies with minimal effort.

## Features
- Send emails to multiple companies with personalized content.
- Embed an image (e.g., a logo) directly in the email body as a signature.
- Attach additional files to each email (optional).
- Option to exit the email-sending process midway if needed.
- Simple and user-friendly prompts for input.

## Prerequisites
- **Google Colab Account**: The script is designed to be run on [Google Colab](https://colab.research.google.com).
- **Gmail Account with App Password**: To send emails, you must create an app password for your Gmail account if you have 2FA enabled.
- **Required Python Packages**: The necessary Python packages are pre-installed in Google Colab.

## Creating an App Password for Gmail (If You Have Two-Factor Authentication Enabled)

### Why You Need an App Password
If you have 2-Step Verification (Two-Factor Authentication) enabled on your Google account, you need to generate an app password to allow this script to send emails on your behalf. This is because Google requires app-specific passwords for applications that access your account via SMTP.

### Steps to Create an App Password
1. **Enable 2-Step Verification**:
   - Go to your [Google Account](https://myaccount.google.com/).
   - Click on **Security** in the left sidebar.
   - Under "Signing in to Google," find **2-Step Verification** and follow the instructions to enable it.

2. **Generate an App Password**:
   - After enabling 2-Step Verification, return to the **Security** section.
   - Under "Signing in to Google," find **App passwords** and click on it.
   - You might need to sign in again for security purposes.
   - In the "Select app" dropdown, choose **Mail**.
   - In the "Select device" dropdown, choose **Other (Custom name)** and name it something like "Email Automation."
   - Click **Generate**.
   - Google will display a 16-character app password. Copy this password and keep it secure.

### Using the App Password in the Script
When prompted for your email password in the script, use the app password you generated instead of your regular Gmail password.

## Setting Up the E-Cell Logo

### Uploading the Logo to Google Colab
The script is designed to embed an E-Cell logo in the email body as a signature. Here’s how to upload and use the logo:

1. **Open Google Colab**: Go to [Google Colab](https://colab.research.google.com) and open your notebook.
2. **Upload the Logo**:
   - On the left sidebar, click the **Files** tab to open the file explorer.
   - Click the **Upload** button and select `ecelllogo.jpg` from your local machine.
   - Ensure the file is uploaded to the `/content/` directory in Colab.
   - The script references the logo using the following path: `/content/ecelllogo.jpg`.

### Customizing the Signature
The signature in the email can be customized to include your own details:

```python
<img src="cid:image1" style="width:100px;height:auto;"><br>
Tejasvitaa Singh,<br>
Senior Executive,<br>
E-Cell, VIT Vellore<br>
Ph:+91 9674573637
