# mini_filesystem
Github link: https://github.com/iremddemir/mini_filesystem
## Disk Manipulation
  1. *mini_fat_create:* Uses fopen with "wb" parameter to create a binary file for both writing and reading mode[1]. fseek is used for creating the file in specified size[2].
  2. *mini_fat_save:* Saves all wanted information in a structred way.
  3. *mini_fat_load:* Assuming the saved structure, reads from saved file and load data
  
  We also implemented helper functions 
  
  4. *mini_fat_find_empty_block*: Iterates the block map to find block with empty type
  5. *mini_fat_read_in_block*: Using fseek function, it is pointed to starting position and reads to buffer from there to specific bytes [3]. 
  6. *mini_fat_write_in_block*: Using fseek function, it is pointed to starting position and writes  into buffer from there 
## File System Manipulation
 1. *mini_file_open:* Does checks for conditions that are required for opening a file. If they are satisfied, it creates a new open file with starting position 0 and other given parameters. Appends open handles.
 2. *mini_file_write:* Does neccesary checks for writing. Uses mini_fat_write_in_block from disk manipulation to write. 
 3. *mini_file_read:* Does neccesary checks for reading. Uses mini_fat_read_in_block from disk manipulation to read. 
## Summary 
Our implementation follows the explanations from project PDF. Our approach was inspecting the completed parts and understanding the logic behind a virtual filesystem to complete implementation. It passes all test cases and it satisfies all wanted properties. Therefore, it runs without a problem.
## References
[1] https://www.ibm.com/docs/en/i/7.1?topic=functions-fopen-open-files
[2] https://man7.org/linux/man-pages/man3/fseek.3.html
[3] https://man7.org/linux/man-pages/man3/fread.3.html
