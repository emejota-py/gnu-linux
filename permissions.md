-----------
PERMISSIONS
-----------
  
  users and groups
    u
      user
        user owner of the file/ directory
    g
      group
      permissions the owner group has
    
    o
      other
        permissions of any other system user

    a
      all the classes
        for all previous classes
  
  meaning
    r = read
    w = write
    x = execute
  
    file
      r
      w
      x

    directory
      r
      w
      x

  permission numbers and their binary relation
    0 = ---
      000
    1 = --x
      001
    2 = -w-
      010
    3 = -wx
      011
    4 = r-
      100
    5 = r-x
      101
    6 = rw-
      110
    7 = rwx
      111

  operator
    +
      assigns more permissions to the indicated class
      only affected rights are overwritten

    -
      removes access permissions to the class

    =
      if the file permissions of a user class are to be renewed, regardless of what rights it had before

      
  commands
    chmod
      $sudo chmod [options] mode file/directory
      #chmod [options] mode file/directory
        $sudo chmod u+x file.txt
        $sudo chmod 700 file.sh

      flags
        -r
          recursive
            the changing access permissions is applied to all files and subdirectories within a folder

        -v
          verbose
            show a diagnosis of all processed files/directories that are been issued

        -c
          changes
            a diagnostic is displayed for all files that have been modified

        -f
          silent
            error messages are silenced

