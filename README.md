# Configuration File Modifier Tool

## Introduction

The **Configuration File Modifier Tool** is a versatile Python script designed to simplify the management and modification of configuration files. By automating the process of editing parameters, enabling commented-out settings, and adding new configurations, this tool is invaluable for system administrators and developers who regularly work with system or application configurations.

---

## Key Features

- **Modify Existing Parameters**: Update existing parameters with new values.
- **Enable Specific Commented Parameters**: Detects commented-out parameters and enables them only if specified for modification.
- **Add Missing Parameters**: Automatically appends new parameters to the configuration file if they are not present.
- **Backup Creation**: Generates a backup of the original file before applying changes, ensuring data safety.
- **Comment Handling**: Processes only actionable lines and skips irrelevant comments.
- **Interactive Input Mode**: Guides users to input configuration details in an easy-to-follow interactive format.

---

## Workflow Overview

1. **File Validation**: The tool checks for the existence of the specified file and aborts the process if the file is missing.
2. **Backup Creation**: A backup of the original file is created with the suffix `_OLD_ModByScript` appended to its name.
3. **Parameter Processing**:
   - Identifies specified parameters.
   - Updates the value of existing parameters.
   - Enables parameters that are commented out but specified for modification.
   - Adds new parameters if they are missing from the file.
4. **Save and Output**:
   - Writes the modified content back to the file.
   - Displays a success message summarizing the changes.

---

## Usage Instructions

### Prerequisites

- Ensure Python 3.x is installed on your system.
- Basic familiarity with configuration file structures is recommended.

### Steps to Run

1. Clone or download the script.
2. Open a terminal and navigate to the script's directory.
3. Run the script:
   ```bash
   python3 ModifyConf.py
   ```
4. Follow the prompts to:
   - Specify the configuration file path.
   - Input parameters and their desired values in the format `parameter=value`.
   - Type `done` to finalize input.

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

Backup created at: /etc/vsftpd.conf_OLD_ModByScript
File '/etc/vsftpd.conf' has been modified.
```

---

## Upcoming Enhancements

- **Parameter Removal**: Introduce the ability to delete parameters from the file.
- **Unified Interface**: Provide users with an integrated option to add, modify, or remove parameters seamlessly.

---

## Credits

- **Author**: CYZ
- **Collaboration**: Developed with the assistance of ChatGPT.

This tool ensures configuration management is both efficient and error-free. Users are encouraged to adapt and extend the script to suit their specific needs.

