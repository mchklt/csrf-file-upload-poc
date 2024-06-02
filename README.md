# CSRF Proof-of-Concept (PoC) for File Upload in Victim Account

This repository contains a proof-of-concept (PoC) demonstrating a Cross-Site Request Forgery (CSRF) attack that uploads a file to a victim's account. The HTML file in this repository dynamically creates and submits a form, including a file upload, using JavaScript.

## Description

This PoC showcases how an attacker can exploit a CSRF vulnerability to upload a file to a victim's account without their knowledge. The attack leverages the victim's session or performs unauthorized actions on their behalf.

The provided HTML file:
1. **Dynamically creates a form**: The form is constructed using JavaScript, ensuring it contains all necessary fields and attributes.
2. **Adds hidden input fields**: These fields mimic the required data for a legitimate form submission, which might include state tokens, user identifiers, and other necessary parameters.
3. **Converts a base64 string to a file**: The file data, initially encoded as a base64 string, is converted to a `Blob` object and then to a `File` object.
4. **Appends the file to the form**: A hidden file input is created and populated with the converted file, simulating a legitimate file upload.
5. **Submits the form automatically**: Upon loading the page, the script submits the form to the specified action URL.

This PoC can be used to understand and demonstrate the mechanics of a CSRF attack involving file uploads, helping security professionals to better protect against such vulnerabilities.

## How It Works

The HTML file executes the following steps:

1. **Create Form**: A form element is created with a specified action URL and method.
2. **Add Hidden Inputs**: Hidden inputs are appended to the form to replicate required form data.
3. **Base64 to File**: A base64-encoded string representing the file is converted to a `Blob` and then to a `File` object.
4. **Create File Input**: A hidden file input is created and the file is assigned to it.
5. **Submit Form**: The form is automatically submitted, uploading the file to the target server.

### Key Points
- **Dynamic Form Creation**: Ensures the form can be easily modified and customized for different targets.
- **Hidden Input Fields**: Mimics legitimate data to bypass basic CSRF protections.
- **File Conversion**: Demonstrates how to handle file uploads within a CSRF attack.

## Usage

To use this PoC:
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/csrf-file-upload-poc.git
   cd csrf-file-upload-poc
2. Read comments and edit !


## NOTE

Read More on my [medium Blog](https://medium.com/@mchklt/self-xss-via-filename-csrf-on-contact-us-multipart-data-form-f852dd539547)
