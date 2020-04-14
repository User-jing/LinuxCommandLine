# LinuxCommandLine

Notes from *Beginning the Linux Command Line* by Sander van Vugt

## Chapter 1

**command + option + argument**
- Options provide a method that is defined within the command code to modify the behavior of the command.
- Many commands offer two different methods of working with options: the short option and the long option
	
  eg. `ls -l -h`  
     	`ls -l —human-readable`
- If more than one option is used, all options can be specified together, without a - in front of each option. So the command `ls -lh` is valid, and so is the command `ls -l -h`.
- Short options are preceded by `-`, long options are preceded by `—-`
- The argument is typically not defined in the command code itself. For example, consider the command `ls -l /etc/hosts`
- You should be aware that not only commands have arguments, but also options have arguments as well

**Piping and Redirection**
- By using piping, you’ll send the result of the first command to the second command. `ls -R / | less`, the `ls -R /` command executes and sends its result to the `less` command
- Another operator that is very useful in the Linux command shell is the redirection operator, `>`.
- `ls -l > file.txt`, you’ll tell the command to send its output to `file.txt`, in this case to a file that has the name somewhere. This file will be created in the current directory if it doesn’t exist. If a file with this name already exists, you will overwrite it by using this command. In case you want to add to an existing file instead of overwriting it, use `ls -l >> file.txt`. The double redirector tells the command to append to the contents of the file instead of overwriting it. If the file doesn’t already exist, the command will create it.
- Some commands give you error messages apart from output, send the error message to `error.txt`. eg `-R 2> error.txt`
- Instead of sending the results of a command to a file, you can redirect to some of the Linux special devices as well. eg. `ls -l 2> /dev/null`
