# Modify-Conf-Files
The Configuration File Modifier Tool is a Python-based utility designed for managing and updating configuration files with ease and precision. It is ideal for use in system administration, server configuration, or any scenario where automated updates to parameterized configuration files are needed.

# Configuration File Modifier Tool

## Overview

The **Configuration File Modifier Tool** is a Python-based script designed for managing and updating configuration files. It simplifies modifying existing parameters, adding new ones, and enabling parameters that are commented out. This tool is ideal for system administrators and developers who work with configuration files regularly.

---

## Features

- **Modify Parameters**: Updates existing parameters with new values.
- **Enable Commented Parameters**: Detects commented-out parameters and enables them.
- **Add Missing Parameters**: Appends new parameters if they do not already exist in the file.
- **Backup Creation**: Automatically creates a backup of the original file before making changes.
- **Comment Handling**: Skips irrelevant comments and only processes actionable lines.
- **Interactive Mode**: Allows users to input parameters interactively during runtime.

---

## Usage Instructions

### 1. Prerequisites

- Python 3.x installed on your system.
- Basic understanding of configuration file structure.

### 2. Running the Script

1. Clone or download the script to your local machine.
2. Open a terminal and navigate to the directory containing the script.
3. Run the script using:
   ```bash
   python3 ModifyConf.py
   ```
4. Follow the interactive prompts:
   - Provide the path to the configuration file you want to modify.
   - Enter parameters and their desired values in the format `parameter=value`.
   - Type `done` when you have finished entering parameters.

### Example Input

- File path: `/etc/vsftpd.conf`
- Parameters:
  ```
  listen=YES
  anonymous_enable=NO
  local_enable=YES
  write_enable=YES
  local_umask=022
  ```

The script will process these parameters, enabling or adding them as necessary.

---

## How It Works

1. **File Validation**:
   - Checks if the specified file exists.
   - Aborts if the file is not found.

2. **Backup Creation**:
   - Creates a backup of the original file with the suffix `_OLD_ModByScript`.

3. **Parameter Modification**:
   - Searches for each specified parameter in the file.
   - Updates the parameter's value if found.
   - If the parameter is commented out, it is uncommented and updated.
   - Appends parameters that are not present in the file.

4. **Output**:
   - Writes the updated content back to the original file.
   - Displays a success message when modifications are complete.

---

## Example Output

```
Enter the path to the file: /etc/vsftpd.conf
Enter the parameters and their values (e.g., 'parameter=value'). Enter 'done' to finish.
Parameter and value: listen=YES
Parameter and value: anonymous_enable=NO
Parameter and value: local_enable=YES
Parameter and value: done

Backup created at: /etc/vsftpd.conf_OLD_ModByScript
File '/etc/vsftpd.conf' has been modified.
```

---

## Upcoming Features

- **Parameter Removal**: Add functionality to remove parameters entirely from the configuration file.
- **Unified Modify/Add/Remove Option**: Provide users with an integrated interface to choose whether to add, modify, or remove parameters.

---

## Credits

- **Author**: CYZ
- **Assistance**: ChatGPT

This tool was crafted to make configuration file management efficient and error-free. Feel free to extend or customize it for your specific needs!

