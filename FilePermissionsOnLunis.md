# File Permissions in Linux

## Project Description
This project demonstrates how to manage file and directory permissions in Linux using command-line tools. You will learn how to check file details, interpret permission strings, and modify permissions for files, including hidden files and directories.

## Check File and Directory Details
To view details about a file or directory, use the `ls -l` command:
```bash
ls -l filename
```
Example output:
```
-rw-r--r-- 1 user user  1234 Mar 25 12:00 myfile.txt
```
To list all files, including hidden ones:
```bash
ls -la
```

## Describe the Permissions String
The permissions string consists of 10 characters:
- The first character represents the file type (`-` for regular files, `d` for directories, `l` for symbolic links, etc.).
- The next nine characters are divided into three sets of three, each representing read (`r`), write (`w`), and execute (`x`) permissions for:
  - The owner
  - The group
  - Others

Example: `-rwxr-xr--`
- `rwx` (owner: read, write, execute)
- `r-x` (group: read, execute)
- `r--` (others: read only)

## Change File Permissions
To modify file permissions, use the `chmod` command.

### Using symbolic notation:
```bash
chmod u+x filename  # Add execute permission for the owner
chmod g-w filename  # Remove write permission for the group
chmod o+r filename  # Add read permission for others
```

### Using numeric (octal) notation:
```bash
chmod 755 filename  # Owner: rwx, Group: r-x, Others: r-x
chmod 644 filename  # Owner: rw-, Group: r--, Others: r--
```

## Change File Permissions on a Hidden File
Hidden files start with a dot (`.`), but they follow the same permission rules.
```bash
chmod 600 .hiddenfile  # Owner: rw-, Group: ---, Others: ---
```
This makes the file accessible only by the owner.

## Change Directory Permissions
To modify directory permissions, use `chmod` with the `-R` flag for recursive changes:
```bash
chmod 755 mydirectory  # Owner: rwx, Group: r-x, Others: r-x
chmod -R 700 mydirectory  # Full access for the owner only
```
The execute (`x`) permission on directories allows users to enter the directory.

## Summary
- Use `ls -l` to check file permissions.
- The permission string consists of file type and three sets of permissions.
- Modify permissions using `chmod` with symbolic or numeric notation.
- Hidden files are managed the same way as regular files.
- Directory permissions impact access and navigation.

By mastering these commands, you gain better control over file security and user access in Linux.

