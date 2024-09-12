


# LS Command Implementation

This project is a custom implementation of the Unix-like `ls` command with several options, providing a detailed and flexible listing of directory contents. It supports listing files and directories in a table format, similar to the behavior of the standard `ls` command.

## Features

- Supports the following `ls` options:
  - **`-l`**: Long format listing, displaying detailed information such as permissions, owner, group, size, and last modification time.
  - **`-a`**: Include all entries, including those starting with a dot (`.`).
  - **`-t`**: Sort by modification time, newest first.
  - **`-u`**: Use access time instead of modification time for sorting.
  - **`-c`**: Use change time instead of modification time for sorting.
  - **`-i`**: Print the index number (inode) of each file.
  - **`-f`**: Disable sorting, list files in directory order.
  - **`-d`**: List directories themselves, not their contents.
  - **`-1`**: Force output to be one entry per line.
- Supports listing the content of one or more directories.
- Organizes the output in a table format for easier readability.

## Usage

The custom `ls` command can be executed with various combinations of the supported options to list the contents of directories in different formats.

### Example Commands

1. **Basic Listing**:
   ```bash
   ./Myls
   ```
   Lists the current directory contents in a simple format.

2. **Long Format with Hidden Files**:
   ```bash
   ./Myls -la
   ```
   Lists all files (including hidden ones) with detailed information.

3. **Sort by Modification Time**:
   ```bash
   ./Myls -lt
   ```
   Lists files sorted by the last modification time, newest first.

4. **List Multiple Directories**:
   ```bash
   ./Myls dir1 dir2
   ```
   Lists the contents of `dir1` and `dir2` in table format.

5. **Combined Options**:
   ```bash
   ./Myls -ltuicfd1
   ```
   Uses all supported options to customize the output format as per the user's requirements.

## Table Format Output

The output is organized in a table format to provide a clear and structured view of the directory contents. Each column represents a different attribute based on the options used (`-l` for detailed format, etc.).

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Myls.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Myls
   ```
3. Compile the code:
   ```bash
   gcc -o Myls main.c functions.c
   ```

## Testing

test the implementation with different combinations of options:
```bash
./Myls -lai
2901318 drwxrwxr-x 3 bassel_mahmoud1 bassel_mahmoud1   4096 Sep 13 00:54 . 
2894225 drwxrwxr-x 7 bassel_mahmoud1 bassel_mahmoud1   4096 Sep 13 01:06 .. 
2908872 drwxrwxr-x 8 bassel_mahmoud1 bassel_mahmoud1   4096 Sep 13 00:54 .git 
2909001 lrwxrwxrwx 1 bassel_mahmoud1 bassel_mahmoud1      6 Sep 13 00:54 bassel -> main.c
2909002 -rw-rw-r-- 1 bassel_mahmoud1 bassel_mahmoud1  12286 Sep 13 00:54 functions.c
2909003 -rw-rw-r-- 1 bassel_mahmoud1 bassel_mahmoud1   1960 Sep 13 00:54 functions.h 
2909004 -rw-rw-r-- 1 bassel_mahmoud1 bassel_mahmoud1   4306 Sep 13 00:54 main.c 
2909005 -rwxrwxr-x 1 bassel_mahmoud1 bassel_mahmoud1  34336 Sep 13 00:54 myls
```





