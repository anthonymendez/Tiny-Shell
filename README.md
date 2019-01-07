# Tiny Shell
## Fall 2018
## ECE373 Assignment 3

### Developers
* [Joshua Howell](https://github.com/Parzival6)
* [Anthony Mendez](https://github.com/anthonymendez)

## Description
Tiny Shell is a tiny shell Unix program created in C. It supports Job Control, and Signal Interrupts.

This program is the third assignment in ECE 373 Software Intensive Engineering. We were given a good amount of helper and wrapper functions, and had to program the following functions:
1. **eval** - Main routine that parses and interprets the command line.
2. **builtin_cmd** - Recognizes and interprets the built-in commands: quit, fg, bg, and jobs.
3. **do_bgfg** - Implements the bg and fg built-in commands.
4. **waitfg** - Waits for a foreground job to complete.
5. **sigchld_handler** - Catches SIGCHILD signals.
6. **sigint_handler** - Catches SIGINT (ctrl-c) signals.
7. **sigtstp_handler** - Catches SIGTSTP (ctrl-z) signals.


## Run and How To Use
1. Run `make`
2. Run `./tsh`
You will be presented with
```
tsh>
```
Now you can run commands just like in a Unix Terminal. To run something basic, like ls, you would type it to **tsh** like so:
```
tsh>/bin/ls -l -d
```
And it should list all the files in the current directory. To run it in the background, add `&` at the end.
```
tsh>/bin/ls -l -d &
```
To see all jobs running in the background, run `jobs`.

To restart a job as the background process run `bg <job>` where <job> is the PID or JID of the job process.

To restart a job as the foreground process run `fg <job>` where <job> is the PID or JID of the job process.

To quit the shell, run `quit`.
