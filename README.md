# mini_filesystem
 ### Small notes about implementation to help create project report:
 1. mini_fat_create:
     fseek too. (tried to use ftruncate but changed it to fseek as in other functions)
2.  mini_fat_save:

3. mini_fat_read_in_block
    fseek to get current position of file, ref: https://man7.org/linux/man-pages/man3/fseek.3.html
    fread to read specified size of bytes, ref: https://man7.org/linux/man-pages/man3/fread.3.html
