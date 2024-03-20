# get-system-information

This bash script, get-system-information.sh, retrieves detailed information about your Linux system's hardware, memory usage, storage, and peripherals.

# Requirements:

This script requires the following commands to be available on your system:

```
lscpu
lsblk
df
lsusb
lspci
free
dmidecode
top (This script launches top in the background, press q to exit)
```

These commands are typically pre-installed on most Linux distributions.  You can verify their availability by running them individually in your terminal. If any are missing, you can install them using your package manager (e.g., sudo apt install lscpu on Debian-based systems).

# Usage:

1. **Download or Clone the Script:** Download the get-system-information.sh script or clone this repository to your desired location.
2. **Make the Script Executable:** Open a terminal, navigate to the directory containing the script, and run the following command:

```
chmod +x get-system-information.sh
```

Use code with caution.

This grants the script permission to execute.

3. **Run the Script:** Execute the script by typing the following command in your terminal:

```
./get-system-information.sh
```

Use code with caution.

# Outputs:

The script will display a comprehensive report containing the following information:

- CPU: Information about your central processing unit (CPU) using lscpu.
- Block Devices: Details about your storage devices using lsblk.
- Filesystem Usage: Disk usage information for mounted filesystems using df -h.
- USB Devices: Information about connected USB devices using lsusb.
- PCI Devices: Details about PCI devices using lspci.
- Memory: Free and used memory information using free -m.
- Memory Details: Information about system memory modules using dmidecode -t memory.
- BIOS Information: Details about the system BIOS using dmidecode -t bios.
- DMI Information: General system information using dmidecode -t.
- System Information: Details about the system hardware using dmidecode -t system.

Note:  The top command is launched in the background to display real-time system resource usage. Press q in the terminal window displaying top to exit.

This script provides a convenient way to gather detailed system information for troubleshooting, system monitoring, or configuration purposes.
