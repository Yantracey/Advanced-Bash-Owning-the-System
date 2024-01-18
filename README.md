# Advanced-Bash-Owning-the-System


In this assignment, the objective was to play the role of a criminal hacker, gaining remote access to a victim's target machine, establishing a backdoor for maintaining access, and subsequently attempting to crack sensitive passwords in the /etc directory. The activity followed the "offense informs defense" philosophy, aiming to enhance understanding of how exploits are carried out and to foster a mindset that helps in protecting against attacks.

The lab environment consisted of an attacker machine and a target machine, with instructions provided to set up access to the target machine. The task was divided into several steps:

**Step 1: Shadow People**

Created a secret user named sysd with a service account appearance, assigned a password, set a system UID and GID, granted full sudo access without a password, and ensured the user did not have a home folder. Tested sysd user's ability to execute commands with sudo access without a password.

**Step 2: Smooth Sailing**

Configured SSH access via port 2222 to provide an alternative backdoor. Edited the /etc/ssh/sshd_config file using Nano to add a secondary SSH port line under port 22.

**Step 3: Testing Your Configuration Update**

Tested the updated configuration by restarting the SSH service, logging off the target machine, and then SSH-ing back in using the sysd user through port 2222.

**Step 4: Crack All the Passwords**

Attempted to crack passwords by SSH-ing into the target machine with the sysd account, escalating privileges to root, and using John to crack the entire /etc/shadow file.

Throughout the assignment, emphasis was placed on learning new tools and concepts, aligning with the philosophy that acquiring knowledge on the job is crucial for IT and security roles. The activities simulated real-world scenarios to better understand the processes involved in maintaining access to a compromised system.
