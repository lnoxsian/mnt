# mnt

**A Bash Script for Managing Disk Partitions**

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Key Controls](#key-controls)
- [Requirements](#requirements)
- [Contributing](#contributing)
- [License](#license)
- [Show Some Love!](#show-some-love)

## Introduction

`mnt` is a user-friendly Bash script designed to simplify the management of disk partitions on Linux systems. Whether you need to mount or unmount partitions, `mnt` provides an intuitive interface to handle these tasks efficiently without the need for complex command-line operations.

## Features

- **Easy Navigation:** Browse through available partitions using arrow keys.
- **Mount & Unmount:** Quickly mount or unmount selected partitions with simple key presses.
- **Custom Mount Points:** Enter a custom mount point interactively, or press <Enter> for auto-mount.
- **Quick Cancel:** Exit the custom mount prompt by entering `q`.
- **Automatic Mount Point Management:** Automatically creates and removes mount points as needed.
- **Supports Multiple Filesystems:** Optimized options for various filesystem types, including `vfat`.
- **Dynamic Updates:** Reflects real-time changes in partition statuses after mount/unmount operations.
- **Clipboard Copy:** Copies the mountpoint of the selected partition to your clipboard.

## Installation

### Step 1: Download the Script

Clone this repository or download the `mnt` script file.

```bash
git clone https://github.com/lnoxsian/mnt.git
cd mnt
```

### Step 2: Copy the Script

You can place the script in `/usr/local/bin` for easy access:

```bash
sudo cp mnt /usr/local/bin/
sudo chmod +x /usr/local/bin/mnt
```

By placing the script in `/usr/local/bin`, you can run it from anywhere in the terminal without specifying the path.

## Usage

Simply run the `mnt` command in your terminal:

```bash
mnt
```

Ensure you have the necessary sudo privileges, as the script requires them to manage mount points.

## Key Controls

- **Up Arrow (`↑`):** Navigate to the previous partition.
- **Down Arrow (`↓`):** Navigate to the next partition.
- **`m` or `M`:** Auto-mount the selected partition at its default location.
- **`e` or `E`:** Prompt to enter a custom mount point:
  - *Press `<Enter>` for auto-mount.*
  - *Enter an absolute path for custom mount.*
  - *Enter `q` to cancel and exit the prompt.*
- **`r` or `R`:** Unmount the selected partition.
- **`d` or `D`:** Copies the mountpoint of the selected partition to the system clipboard.
- **`q` or `Q`:** Quit the script.

### Example Interface

```
------------------------------------------------------------------------------------------
NAME       LABEL                SIZE       TYPE       MOUNTPOINT         
------------------------------------------------------------------------------------------
  sda1      System               100G      part      /mnt/system        
> sda2      Data                 500G      part      -
  sdb1      Backup               250G      part      /mnt/backup        
------------------------------------------------------------------------------------------
Press 'm' to auto mount, 'e' for custom mount, 'r' to unmount, 'd' to copy, 'q' to quit.
```

In this example, the currently selected partition is highlighted with a `>` symbol. Use the arrow keys to change the selection and press the corresponding key to perform actions.

## Requirements

- **Operating System:** Linux
- **Shell:** Bash
- **Permissions:** Sudo privileges are required to execute mount and unmount operations.
- **Dependencies:** Utilizes standard Linux utilities like `lsblk`, `blkid`, `mount`, `umount` and `xclip`, `xsel`, or `wl-copy`.

## Contributing

Contributions are welcome! If you have suggestions, bug reports, or want to contribute code, please open an issue or submit a pull request on [GitHub](https://github.com/lnoxsian/mnt).

## License

This project is licensed under the [GPL License](LICENSE).

---

**Disclaimer:** Use this script at your own risk. Ensure you understand the implications of mounting and unmounting partitions to prevent data loss.

---

## Show Some Love!

🌟 **Special thanks to [@TaluKara](https://github.com/TaluKara), creator of the original `mnt` script!**  
If you find this project helpful, please check out and support the original upstream repo here:

👉 [Original mnt by TaluKara](https://github.com/TaluKara/mnt)

Go give it a star, leave feedback, and show some appreciation for the dedication and open source spirit!  
If you are using or building on this code, it's always cool to recognize and support the pioneers that made it possible.
