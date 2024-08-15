

# Terraform Installation on Windows Using Chocolatey

## Introduction
This guide provides a step-by-step process for installing Terraform on a Windows machine using the Chocolatey package manager via the command line. Terraform is an open-source infrastructure as code software tool that provides a consistent CLI workflow to manage cloud services.

## Prerequisites
- Windows 7 or newer.
- Administrator access on the Windows machine.
- Internet connection.

## Step 1: Install Chocolatey via Command Line
Chocolatey is a package manager for Windows that simplifies software installation and management.

1. **Open Command Prompt as Administrator**:
   - Press `Windows + X`, then select `Command Prompt (Admin)` or `Windows Terminal (Admin)`.

2. **Run the Following Command to Install Chocolatey**:
   - Copy and paste the command below into the command prompt and press `Enter`:
   ```cmd
   @powershell -NoProfile -ExecutionPolicy Bypass -Command "Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
   ```
   - This command sets the execution policy to bypass, downloads the Chocolatey installation script, and runs it.

3. **Verify Chocolatey Installation**:
   - After installation, verify that Chocolatey is installed correctly by running:
   ```cmd
   choco -v
   ```
   - The output should display the installed version of Chocolatey.

## Step 2: Install Terraform Using Chocolatey

1. **Install Terraform**:
   - With Chocolatey installed, run the following command to install Terraform:
   ```cmd
   choco install terraform -y
   ```
   - The `-y` flag automatically confirms the installation, so you don’t have to manually approve it.

2. **Verify Terraform Installation**:
   - After installation, verify that Terraform is installed correctly by running:
   ```cmd
   terraform -v
   ```
   - The output should display the installed version of Terraform.

## Conclusion
Terraform is now successfully installed on your Windows machine using Chocolatey. You can begin managing your infrastructure as code. For more information on Terraform, visit the [official Terraform documentation](https://www.terraform.io/docs).
