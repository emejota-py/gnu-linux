# PERMISSIONS

## Users and groups
* `u` (user) User owner of the file/directory.
* `g` (group) Permissions the owner group has.
* `o` (other) Permissions of any other system user.
* `a` (all the classes) For all previous classes.

## Meaning
* `r` = Read.
* `w` = Write.
* `x` = Execute.

Diferences between files and directories:

* File
  * `r`
  * `w`
  * `x`
* Directory
  * `r`
  * `w`
  * `x`

## Permission numbers and their binary relationship

| Decimal | Permissions | Binary| 
|:-------:| :----------:|:-----:| 
|    0    |     ---     |  000  | 
|    1    |     --x     |  001  | 
|    2    |     -w-     |  010  | 
|    3    |     -wx     |  011  |
|    4    |     r--     |  100  | 
|    5    |     r-x     |  101  |
|    6    |     rw-     |  110  | 
|    7    |     rwx     |  111  | 

## Operators
* `+` Assigns more permissions to the indicated class
only affected rights are overwritten.
* `-` Removes access permissions to the class.
* `=` If the file permissions of a user class are to be renewed, regardless of what rights it had before.

## Commands
### chmod
```sh
$sudo chmod [options] mode file/directory
#chmod [options] mode file/directory

$sudo chmod u+x file.txt
$sudo chmod 700 file.sh
```
* chmod
  * Flags
    * `-r` (recursive) The changing access permissions is applied to all files and subdirectories within a folder.
    * `-v` (verbose) Show a diagnosis of all processed files/directories that are been issued.
    * `-c`(changes) A diagnostic is displayed for all files that have been modified.
    * `-f` (silent) The error messages are silenced.
