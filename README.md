# mini_filesystem
 ### Small notes about implementation to help create project report:
 1. mini_fat_create:
     ftruncate to create a file of predetermined size, ref: https://man7.org/linux/man-pages/man3/ftruncate.3p.html
2.  mini_fat_save:

3. mini_fat_read_in_block
    fseek to get current position of file, ref: https://man7.org/linux/man-pages/man3/fseek.3.html
    fread to read specified size of bytes, ref: https://man7.org/linux/man-pages/man3/fread.3.html
