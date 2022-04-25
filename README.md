# Monitoring-101

##### The Mission
One of the most important responsibilities a system administrator has, is monitoring the systems he manages. Indeed it's one thing to set them up and install software on them, but then what!? Well the next step is ensuring that the machines you provisioned as well as the services you deployed on them remain available, reliable and secure!

This challenge is divided in two tasks, the first one having you research how to monitor a Linux system as well as what to look for when doing so. You will have to take note of all your findings in a text file (EX: markdown) while being as exhaustive as possible (what to monitor, how to monitor it, commands used, ...). Try to answer, but don't limit yourself to, the questions below to guide you through the research process:

- What are the main area of concern when monitoring a system? (EX: CPU load, disk usage, ...)
---------
- How can you check what are the most memory intensive running processes? [Find top running process by memory usage](https://www.linuxshelltips.com/find-top-running-processes-by-memory-usage/)

*You will use the **top** command-line utility, which is a task manager in Unix and Linux systems that shows all the details about running processes.*

To show the most memory consuming processes, we make use of the **'-o'** flag at the top to sort the output.

 top -o %MEM   - command to find the process using highest memory usage

-----------------
- What are log files? Where can you fin them on a typical Linux system?

LOG is the file extension for an automatically produced file that contains a record of events from certain software and operating systems. While they can contain a number of things, log files are often used to show all events associated with the system or application that created them. For example, your backup program might keep log files showing exactly what happened (or didn’t happen) during a backup. Windows keeps all kinds of log files for its various services.

The point of a log file is to keep track of what’s happening behind the scenes and if something should happen within a complex system, you have access to a detailed list of events that took place before the malfunction. Basically, whatever the application, server, or OS thinks needs to be recorded.

While most log files contain the .log file extension, sometimes applications may use the .txt extension or a different proprietary extension, instead.

*Almost all logfiles are located under **/var/log** directory and its sub-directories on Linux. You can change to this directory using the **cd command**.*

---------------
- How can you check who where the last connected users, what they did, when they left?
-----------
- What are the different metrics of health and performance of a system?

*Metrics used for monitoring*

~ CPU – It is crucial to monitor CPU, as it can reach a high utilization rate and temperature. It can have multiple cores, but an application can be directed to only one of these cores, pointing to a dangerous hardware behavior. (Central processing unit)

~ Load – This specifies whether the CPU is being used, how much is being executed, and how long it has been running.

~ Disk Capacity and IO – Disk capacity is especially important when it comes to image servers, files, and VMs, as it can directly affect system shutdown, corrupt the operating system, or cause extreme IO slowness. Along with disk monitoring, it’s possible to plan for an eventual change or addition of a disk, and to verify the behavior of a disk that demonstrates signs of hardware failure.

~ Network – When it comes to DNS, DHCP, firewall, file server, and proxy, it is extremely important to monitor network performance as input and output of data packets. 
With network performance logs, you can measure the utilization of the card, and create a plan to suit the application according to the use of the network.

~ Memory – Memory monitoring in other components determines the immediate stop of a system due to memory overflow or misdirection for a single application.

~ Swap – This is virtual memory created by the system and allocated to disk to be used when necessary. Its high utilization can indicate that the amount of memory for the server is insufficient.
 
----------------------------------
- How can you check the uptime of a machine? [Check windows uptime](https://www.minitool.com/news/how-to-check-windows-uptime.html)

Uptime means the time your machine has been running till now. It is actually a measure of system reliability to show you exactly how long your computer has been working and available since last startup.

###### Find Windows Uptime in Task Manager
1. Move your cursor onto the taskbar, and then right click on it. (Solve the Windows 10 taskbar not working issue.)
1. Choose Task Manager from the context menu you see.
1. If you see a small Task Manager window, please click More details. (If you see a full window, skip this step.)
1. Shift to the Performance tab.
1. Keep the CPU option checked in the left sidebar.
1. Look at the bottom left section in the right pane.
1. The Up-time value will shows in days: hours: minutes: seconds in real-time.

##### Check System Uptime through PowerShell
1. Right click on the Windows button in the lower left corner of your PC screen.
1. Choose Windows PowerShell or Windows PowerShell (Admin) from the list.
1. Type (get-date) – (gcim Win32_OperatingSystem).LastBootUpTime into PowerShell window and press Enter on the keyboard.
1. Now, you can see how much time your PC is running in total (days, hours, minutes and seconds are displayed separately).

-----------------------
- How can you assess the network traffic?

The second task is meant to serve as practice and will have you, in a different file, write a report with as many relevant information (what would make sense in a report) as you can muster on a system you manage. It most preferably would be a remote machine, but it can also be your local machine as this is just practice.

To validate the challenge you will have to make a pull request containing both files (research notes and system report) in this folder of your training's repository.

IMPORTANT: Take your time when researching, it's the most important part of this challenge as you'll need to be able to find out what is happening on any given system at any given time. Whether it's the percentage of system's resources currently used, what commands are being run, who is logged in, and so on...

-------------
##### Complimentary resources
[Monitoring commands](https://www.ubuntupit.com/most-comprehensive-list-of-linux-monitoring-tools-for-sysadmin/)

[Linux system monitoring fundamentals](https://www.linode.com/docs/guides/linux-system-monitoring-fundamentals/)
