
# Algorithm for File Updates in Python

## Project Description

This project automates the process of updating an "allow list" of IP addresses stored in a file. The goal is to remove specific IP addresses that are listed in a separate "remove list". The algorithm ensures that only valid, necessary IPs remain in the allow list, supporting tasks such as network access management or firewall configurations.

## Open the File that Contains the Allow List

The file is accessed using Python's built-in `open()` function in read mode (`'r'`). This allows us to retrieve the current list of allowed IP addresses:

```python
file = open("allow_list.txt", "r")
data = file.read()
file.close()
```

## Read the File Contents

The content of the file, expected to be a comma-separated string of IP addresses, is read and stored in a variable:

```python
print(data)
# Example output: '192.168.0.1,192.168.0.2,10.0.0.1'
```

## Convert the String into a List

The string is split into individual IP addresses using the `split()` method:

```python
allow_list = data.split(",")
```

This gives a list of strings:

```python
['192.168.0.1', '192.168.0.2', '10.0.0.1']
```

## Iterate Through the Remove List

We define a separate list of IP addresses that we want to remove:

```python
remove_list = ['192.168.0.2', '10.0.0.1']
```

We use a `for` loop to iterate through the `remove_list`, and use `.remove()` to eliminate matching IPs from the `allow_list`:

```python
for ip in remove_list:
    if ip in allow_list:
        allow_list.remove(ip)
```

## Remove IP Addresses That Are on the Remove List

After the loop executes, the `allow_list` is now updated:

```python
print(allow_list)
# Output: ['192.168.0.1']
```

## Update the File with the Revised List of IP Addresses

We write the updated IP list back to the original file using `.write()`:

```python
file = open("allow_list.txt", "w")
file.write(",".join(allow_list))
file.close()
```

## Summary

This algorithm:
- Uses `.read()` to extract content from a file.
- Splits the content into a list.
- Iterates with a `for` loop through a remove list.
- Removes matching entries using `.remove()`.
- Uses `.write()` to overwrite the file with the updated list.

This step-by-step method maintains clarity while leveraging basic file and list operations in Python.
