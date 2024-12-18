# Splunk Config Fix

This repository documents the resolution of a permissions issue caused by changes to the `config.conf` file in a Splunk setup. The error prevented access to logs and required manual corrections. Below are the details and steps taken to resolve the issue.

## Problem Description
An incorrect modification to the `config.conf` file altered certain permissions, blocking access to Splunk logs. This issue required identifying the misconfigured file, restoring proper permissions, and ensuring access was restored.

## Steps to Fix the Issue

1. **Locate the `config.conf` File**
   - Use Splunk’s file structure to find the `config.conf` file in the affected directory.
   - Example path: `SPLUNK_HOME/etc/system/local/config.conf`

2. **Edit the File**
   - Open the file using a text editor (e.g., `vi`, `nano`, or Notepad++).
   - Review and correct any misconfigurations, ensuring the appropriate permissions are set.

3. **Copy the File**
   - Backup the original file before applying changes.
   - Replace the misconfigured file with the corrected version.
   - Example command:
     ```bash
     cp config.conf /correct/location/
     ```

4. **Restart Splunk**
   - Restart the Splunk service to apply the changes:
     ```bash
     splunk restart
     ```

## Repository Contents
- **Original Config File**: A sample of the misconfigured `config.conf` file.
- **Corrected Config File**: The updated version with proper permissions.
- **Troubleshooting Guide**: Best practices for preventing similar issues in the future.

## Lessons Learned
- Always back up configuration files before making changes.
- Use version control to track changes to critical files like `config.conf`.
- Regularly review permissions and access controls in Splunk to ensure they align with organizational policies.


