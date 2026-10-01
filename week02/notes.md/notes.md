Lab 1 Notes: The Terminal

1. What did pwd print?
It printed the absolute path of the current working directory starting from the root directory.

2. What did ls -a show that plain ls did not?
It showed hidden files and directories, which are files beginning with a dot (`.`), including `.` (current directory) and `..` (parent directory).

 3. Pick one line from ls -l. What do you think the first column means?
The first column  represents file type and permissions. The first character indicates whether it is a regular file  or directory , followed by read , write , and execute  permissions for the owner, group, and others.

 4. Why does that work from where you are standing? Which kind of path is coding-cafe/week02? Absolute or Relative?
It works because `coding-cafe` is located directly inside the current working directory. It is a **relative path** because it resolves relative to the current working directory rather than starting from root .

 5. mv did two different jobs above. What were they?
First, `mv` moved a file into a different directory (`week01/`). Second, `mv` renamed a file (`README-backup.md` to `old-readme.md`).

 6. How many folders are on your PATH?
There are 7 folders on my PATH (determined by running `echo $PATH` and counting the paths separated by colons `:`).

 7. Write down exactly where your python3 lives.
`/usr/bin/python3`

 8. Compare your answer to 7 with the person next to you. Are they the same? If not, why might that be?
They are the same, but if they differed, it would be due to different installation methods

 9. What exactly did the shell say? Explain the error in your own words, using the word PATH.
The shell returned `command not found: pyton3`. The shell checked every directory listed in the `PATH` environment variable in order, found no executable file named `pyton3`, and reported that the command could not be located.

 10. .venv did not appear with plain ls. Why not?
The directory name `.venv` starts with a leading dot (`.`), which marks it as a hidden folder in Unix-based operating systems. Plain `ls` ignores hidden files.

 11. What changed about your prompt?
The prefix `(.venv)` appeared at the beginning of the terminal prompt line, indicating the virtual environment is currently active.

 12. Compare this with what you wrote down for question 7. Is it the same path? If not, what does that tell you about what activate actually did to your PATH?
It is not the same path; `which python3` now points to `.../coding-cafe/.venv/bin/python3`. This shows that the `activate` script prepended the virtual environment's `bin/` directory to the `PATH` variable so the environment's Python binary is prioritized.

 13. What is in the second list that was not in the first?
The second list includes `requests` along with its dependencies: `certifi`, `charset-normalizer`, `idna`, and `urllib3`.

 14. Where does python3 point now?
It points back to the system Python at `/usr/bin/python3` because running `deactivate` restored the original system `PATH`.

 15. Find what ls -h does. Write it in your own words.
The `-h` option stands for human-readable; when used with `-l`, it displays file sizes using readable units (like K, M, G) instead of plain byte counts.

 16. What is the difference between what Ctrl+C and Ctrl+D did?
 Ctrl +c sends a signal to immediately kill the running process, whereas Ctrl + D send end of file signal to close input stream or exit the session.


