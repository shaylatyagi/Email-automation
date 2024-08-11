# Email-automation
A Python script for automating email sending with attachments and embedded images.
## Using the E-Cell Logo

The script is designed to embed an image (e.g., a logo) in the email body as a signature. A sample logo file, `ecelllogo.jpg`, is provided in this repository. Follow the steps below to use it:

### 1. Upload the Logo to Google Colab
- In your Google Colab notebook, go to the **Files** tab on the left-hand side.
- Click the **Upload** button and select `ecelllogo.jpg` from your local machine.
- Ensure the file is uploaded to the `/content/` directory in Colab.

### 2. Reference the Logo in the Script
- The script automatically references the logo from the `/content/` directory with the following path:
  ```python
  image_path = "/content/ecelllogo.jpg"
