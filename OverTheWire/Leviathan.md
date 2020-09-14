## Leviathan - Basic Unix Vulnerabilities

## Level 0 - Hidden Directories

Directories that start with `.` are hidden by default when viewing a the contents of a directory. Running `ls -a` will show all folders, and allow you to access items that are otherwise hidden. This level had a hidden backups folder, that contained a file with the password

The password for level 1 is `rioGegei8m`

## Level 1 - Tracing System/Library Calls

This level contains a binary called `check` in the home directory. Running it opens a prompt for a password, which just tells me I have given it the wrong password when I just pass it "a". When I run strings I find a few strings nearby the password prompt, but none of them work. I then try debugging the binary with `strace` to debug sytem calls, and see that it reads from `stdio`, but there is no checking the password against any files or anything. I then debugged it with `ltrace` to detect standard library calls, which reveals a string compare to a string, which when passed as the password it opens up a shell. When I run `id` in that shell it reveals that I have the uid of `leviathan2`, so when I cat the password in `/etc`, it reveals the password.

The password for level 2 is `ougahZi8Ta`

## Level 3 - Symlinks and Exploiting System Calls

This level features an executable called `printfile`, that when triggered with a path to a file in ltrace, we see that it checks the permission of the given file, then executes `cat` on that file. Based on reading details of the `access` library call and details of the `cat` command, we see that if we pass a string with a space (ex. call it with `./printfile "a b"`) then `access` will behave differently than `cat`. `access` will check access for a file called "a b", whereas `cat` will print out files `a` and `b`. To make it easier I created a file called `a` with a basic string inside, and a file named `b` that is a symlink to the password file for level 3. I then ran `printfile "a b"` which revealed the password.

The password for level 3 is `Ahdiemoo1j`

## Level 4 - Reviewing System/Library Calls

This level features an executable called `level3`. When run with `ltrace` it shows that it prompts for a password, and then compares it to "snlprintf". When I exit `ltrace` and execute it normally, I am able to pass that password in and get access to a shell which is able to print the contents of the password file.

The password for level 4 is `vuH0coox6m`