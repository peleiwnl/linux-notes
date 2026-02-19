Every time you launch an application, or execute a command, the system creates a process for it. This involves controlling and monitoring all the running programs on the system. The kernel is in charge of managing these processes, making sure they get the right resources and run smoothly on the CPU. 

There are two types:
1. <span style="color:rgb(24, 205, 136)"><b>Foreground processes</b>:</span> Also known as interactive processes. They are executed/initiated by the user or the programmer, not system services. They take input from the user and return the output. We cannot directly initiate a new process from the same terminal while these are running
2. <span style="color:rgb(24, 205, 136)"> <b>Background processes</b></span>: Non-interactive processes. Executed or initiated by the system itself or by users, though they can be managed by users. These processes have a unique PID or process if assigned to them, and we cannot initiate other processes within the same terminal from which they are initiated.

## Process States

Processes go through several states in their lifetime, helping the system track what each process is doing:

- [[created]]
- [[ready]]
- [[running]]
- [[sleeping]]
- [[stopped]]
- [[zombie]]
- [[orphan]]
- [[terminated]]

## Managing Processes

- The `sleep (number)` command for waiting
- To get a list of jobs running/stopped, use the `jobs` command
- To run all pending and force stopped jobs in the background, use the `bg` command
- To get the details of a process running in the background, use the `ps -ef | grep sleep` command
- To run all the pending and forced stopped jobs in the foreground, use the `fg` command
- To run a process in the background without getting impacted by closing the terminal, run the `nohup sleep 100 &` command
- To run some processes in the background directly, use the `sleep 100&` command
- To run processes with priority, run the `nice -n 5 sleep 100` command
- To get a list of all running processes on the Linux machine, use [[top]] command.






