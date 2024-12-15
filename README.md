# Configuration File Modifier Tool

## Introduction

The **Configuration File Modifier Tool** is a versatile Python script designed specifically for Linux systems to simplify the management and modification of configuration files. By automating the process of editing parameters, enabling commented-out settings, and adding new configurations, this tool is essential for system administrators and developers who work with Linux-based configurations.

---

## Key Features

- **Modify Existing Parameters**: Seamlessly update existing configuration parameters with new values.
- **Enable Specific Commented Parameters**: Automatically detects commented-out parameters and enables them only if specified for modification.
- **Add Missing Parameters**: Appends new parameters to the configuration file if they do not already exist.
- **Backup Creation**: Creates a secure backup of the original file with a timestamp before making changes.
- **Comment Handling**: Intelligently processes only actionable lines and skips irrelevant comments to maintain clarity.
- **Interactive Input Mode**: Provides a modern, user-friendly interface to input configuration details interactively.

---

## Workflow Overview

1. **File Validation**: Ensures the specified file exists and aborts the process if the file is missing.
2. **Backup Creation**: Automatically creates a backup of the original file with the suffix `_OLD_ModByScript` and includes a timestamp for easy identification.
3. **Parameter Processing**:
   - Identifies and processes the specified parameters.
   - Updates the value of existing parameters.
   - Enables parameters that are commented out but specified for modification.
   - Adds new parameters if they are missing from the file.
4. **Save and Output**:
   - Writes the modified content back to the file.
   - Displays a clear success message summarizing the changes.

---

## Usage Instructions

### Prerequisites

- **Linux System**: This tool is specifically designed for Linux-based configuration files.
- **Python 3.x Installed**: Ensure Python 3.x is available on your system.
- **Basic Configuration Knowledge**: Familiarity with configuration file structures is recommended.

### Steps to Run

1. Clone or download the script to your Linux system.
2. Open a terminal and navigate to the script's directory.
3. Run the script using:
   ```bash
   python3 ModifyConf.py
   ```
4. Follow the interactive prompts:
   - Specify the full path to the configuration file.
   - Input parameters and their desired values in the format `parameter=value`.
   - Type `done` to finalize the input and apply changes.

---

## Example

### Input

File Path: `/etc/vsftpd.conf`

Parameters:
```plaintext
listen=YES
anonymous_enable=NO
local_enable=YES
write_enable=YES
local_umask=022
```

### Output

```plaintext
Enter the path to the file: /etc/vsftpd.conf
Enter the parameters and their values (e.g., 'parameter=value'). Enter 'done' to finish.
Parameter and value: listen=YES
Parameter and value: anonymous_enable=NO
Parameter and value: local_enable=YES
Parameter and value: done

Backup created at: /etc/vsftpd.conf_OLD_ModByScript_20241215
File '/etc/vsftpd.conf' has been successfully modified.
```

---

## Upcoming Enhancements

- **Parameter Removal**: Add the ability to delete parameters from configuration files for better flexibility.
- **Unified Interface**: Introduce an integrated option to allow users to add, modify, or remove parameters seamlessly.
- **Enhanced Logging**: Implement detailed logging for better traceability of changes.

---

## Credits

- **Author**: CYZ
- **Collaboration**: Developed with the assistance of ChatGPT.
- yes i like to snitch myself out ( i'm not that good (or it would have took me a days or two ))

This tool is a modern solution for Linux system configuration management, ensuring efficiency, reliability, and user-friendly operation. Feel free to adapt or extend this script to meet your specific needs.

