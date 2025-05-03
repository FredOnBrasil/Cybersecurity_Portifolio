
# Algorithm for File Updates in Python

## Project Description

This project automates the process of updating an "allow list" of IP addresses stored in a file. The goal is to remove specific IP addresses that are listed in a separate "remove list". The algorithm ensures that only valid, necessary IPs remain in the allow list, supporting tasks such as network access management or firewall configurations.

## Open the File that Contains the Allow List

The file is accessed using Python's built-in `open()` function in read mode (`'r'`). This allows us to retrieve the current list of allowed IP addresses:

```python
with open("allow_list.txt", "r") as file:
    data = file.read()
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

A separate list, `remove_list`, contains the IPs that need to be deleted from the allow list. We loop through this list:

```python
remove_list = ['192.168.0.2', '10.0.0.1']
```

## Remove IP Addresses That Are on the Remove List

Using a list comprehension, we filter out IPs that appear in `remove_list`:

```python
updated_list = [ip for ip in allow_list if ip not in remove_list]
```

This results in:

```python
['192.168.0.1']
```

## Update the File with the Revised List of IP Addresses

We write the updated IP list back to the original file, joining the list into a comma-separated string:

```python
with open("allow_list.txt", "w") as file:
    file.write(",".join(updated_list))
```

## Summary

This algorithm:
- Reads a list of IP addresses from a file.
- Converts the string into a list format.
- Iteratively compares each entry with a predefined remove list.
- Removes matching entries.
- Writes the cleaned-up list back to the original file.

This approach is efficient, readable, and adaptable for various file-based filtering tasks.
