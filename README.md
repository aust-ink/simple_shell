<h1>0x16. C - Simple Shell</h1>
<p>Write a simple UNIX command interpreter.</p>

<h2>man or help:</h2>
<ul>
<li>sh (Run sh as well)</li>
</ul>

<h2>Output</h2>
<ul>
<li>Unless specified otherwise, your program must have the exact same output as sh (/bin/sh) as well as the exact same error output.</li>
<li>The only difference is when you print an error, the name of the program must be equivalent to your argv[0]</li>
</ul>
  
<p>Example of error with sh: <br>
$ echo "qwerty" | /bin/sh <br>
/bin/sh: 1: qwerty: not found <br>
$ echo "qwerty" | /bin/../bin/sh <br>
/bin/../bin/sh: 1: qwerty: not found <br>
$ </p> 

<p>Same error with your program hsh: <br>
$ echo "qwerty" | ./hsh <br>
./hsh: 1: qwerty: not found <br>
$ echo "qwerty" | ./././hsh <br>
./././hsh: 1: qwerty: not found <br>
$ </p>

<h2>List of allowed functions and system calls</h2>
<ul>
  <li>access (man 2 access)</li>
  <li>chdir (man 2 chdir)</li>
  <li>close (man 2 close)</li>
  <li>closedir (man 3 closedir)</li>
  <li>execve (man 2 execve)</li>
  <li>exit (man 3 exit)</li>
  <li>_exit (man 2 _exit)</li>
  <li>fflush (man 3 fflush)</li>
  <li>fork (man 2 fork)</li>
  <li>free (man 3 free)</li>
  <li>getcwd (man 3 getcwd)</li>
  <li>getline (man 3 getline)</li>
  <li>getpid (man 2 getpid)</li>
  <li>isatty (man 3 isatty)</li>
  <li>kill (man 2 kill)</li>
  <li>malloc (man 3 malloc)</li>
  <li>open (man 2 open)</li>
  <li>opendir (man 3 opendir)</li>
  <li>perror (man 3 perror)</li>
  <li>read (man 2 read)</li>
  <li>readdir (man 3 readdir)</li>
  <li>signal (man 2 signal)</li>
  <li>stat (__xstat) (man 2 stat)</li>
  <li>lstat (__lxstat) (man 2 lstat)</li>
  <li>fstat (__fxstat) (man 2 fstat)</li>
  <li>strtok (man 3 strtok)</li>
  <li>wait (man 2 wait)</li>
  <li>waitpid (man 2 waitpid)</li>
  <li>wait3 (man 2 wait3)</li>
  <li>wait4 (man 2 wait4)</li>
  <li>write (man 2 write)</li>
</ul>

<h2>Compilation</h2>
<p>Your shell will be compiled this way:</p>
<p>gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh</p>

<h2>Testing</h2>
<p>Your shell should work like this in interactive mode: <br>
$ ./hsh <br>
($) /bin/ls <br>
hsh main.c shell.c <br>
($) <br>
($) exit <br>
$ </p>

<p>But also in non-interactive mode: <br>
$ echo "/bin/ls" | ./hsh <br>
hsh main.c shell.c test_ls_2 <br>
$ <br>
$ cat test_ls_2 <br>
/bin/ls <br>
/bin/ls <br>
$ <br>
$ cat test_ls_2 | ./hsh <br>
hsh main.c shell.c test_ls_2 <br>
hsh main.c shell.c test_ls_2 <br>
$ </p>

<h2>Tasks</h2>

<h3>0. Betty would be proud</h3>
<p>Write a beautiful code that passes the Betty checks</p>

<h3>1. Simple shell 0.1</h3>
<p>Write a UNIX command line interpreter.</p>
<ul>
  <li>Usage: simple_shell</li>
</ul>

<p>Your Shell should:</p>
<ul>
<li>Display a prompt and wait for the user to type a command. A command line always ends with a new line.</li>
  <li>The prompt is displayed again each time a command has been executed.</li>
<li>The command lines are simple, no semicolons, no pipes, no redirections or any other advanced features.</li>
  <li>The command lines are made only of one word. No arguments will be passed to programs.</li>
  <li>If an executable cannot be found, print an error message and display the prompt again.</li>
  <li>Handle errors.</li>
  <li>You have to handle the “end of file” condition (Ctrl+D)</li>
</ul>  
  
<p>You don’t have to:</p>
<ul>
  <li>use the PATH</li>
  <li>implement built-ins</li>
  <li>handle special characters : ", ', `, \, *, &, #</li>
  <li>be able to move the cursor</li>
  <li>handle commands with arguments</li>

  <h3>2. Simple shell 0.2</h3>
<p>Simple shell 0.1 +</p>
<ul>
  <li>Handle command lines with arguments</li>
  </ul>
  
  <h3>3. Simple shell 0.3</h3>
  <p>Simple shell 0.2 + </p>
<ul>
  <li>Handle the PATH</li>
  <li>fork must not be called if the command doesn’t exist</li>
  </ul>
  
  <h3>4. Simple shell 0.4</h3>
  <p>Simple shell 0.3 +</p>
<ul>
  <li>Implement the exit built-in, that exits the shell</li>
  <li>Usage: exit</li>
  <li>You don’t have to handle any argument to the built-in exit</li>
  </ul>
  
  <h3>5. Simple shell 1.0</h3>
  <p>Simple shell 0.4 +</p>
<ul>
  <li>Implement the env built-in, that prints the current environment</li>
  </ul>
  
