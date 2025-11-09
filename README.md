# A Simple Bash Menu for Admin Tasks

This is a simple suite of Bash scripts I put together for a project. The goal is to automate a few common system maintenance tasks from one central menu.
It's not super fancy, but it gets the job done.

## What it Does:

It's a main menu that launches other scripts to do a few different things:

* **Automated Backups:** Runs a script to make a backup of your files.
* **System Updates:** Kicks off another script to update system packages and do a quick cleanup.
* **Log Monitoring:** Scans system logs to find and alert you about certain errors or keywords.

I also added some basic error handling and logging to each script so you can see what it did (or why it failed).

## How to Use:

### Clone the repo:

Bash

git clone [https://github.com/Ansuman942/SysMaint-Project.git](https://github.com/Ansuman942/SysMaint-Project.git)


cd SysMaint-Project

### Set up your config (Important!)

Before you run it, you'll need to open `backup.sh` and change the source/destination directories to match your system.
You might also want to look at `log_monitor.sh` to change which log file it's watching or what keywords it's looking for.

### Run the main menu:

### Bash
bash main.sh


This will bring up the menu, and you can just pick the task you want to run.
### Heads Up: Sudo Required
You'll need sudo (admin) permissions to run a couple of these scripts:
The Update Script needs it to actually install updates.

The Log Monitor will probably need it to read protected system logs.

The menu script is set up to ask for your password when you run those tasks.
