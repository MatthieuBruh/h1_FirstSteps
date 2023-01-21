# Table of contents
1. [ Summary. ](#summary)
2. [ Solve. ](#solve)
3. [ Hacker warmup. ](#warmup)

<a name="summary"></a>
# Summary
### [Hutchins et al 2011: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains](https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf)

## Abstract

* Generally, defense tools (intrusion detection and anti-virus) focus on the vulnerable component of risk. This kind of tools also relies on the fact that an intrusion is successful
* There is now a new type of threat named "Advanced Persistent Threat" (APT). In this category, we have some adversaries that are well-resourced and trained. They conduct intrusion campaigns during years and which affect sensitive economic or national security information. To achieve their goals, they use advanced tools and techniques that bypass conventional security methodologies
* By using some network defense techniques that use the knowledge about APT, you allow defenders to create a feeder loop of intelligence that leads them to achieve a state of information superiority, which reduces the adversary's probability of success with each new intrusion attempt.
* The utilization of a kill chain model to outline the stages of intrusions, correlating the adversary's attack chain indicators with defensive measures, recognizing patterns that connect individual breaches to larger campaigns, and recognizing the cyclical nature of intelligence collection are the foundation of intelligence-based computer network defense (CND).
* Because of the evolution of the threads, it is necessary to use an intelligence-based model. With this kind of model, the defenders don't only mitigate the component of risk. 


## 3.2 Intrusion Kill Chain

* We use kill chain as a systematic process to target and engage an adversary to create desired effects.
  * We also use kill chain in the military domain as the U.S. military with their targeting process: find, fix, track, target, engage, asses (F2T2EA).
  * A kill chain is a end-to-end process, because if one step fails, it will interrupt the entire process.
* By using the previous base, a kill chain has been developed especially for the intrusions. It is based on the fact that an intrusion involves that the aggressor has to develop enough power to be able to establish a presence inside trusted environment.
 * This kill chain is composed of the following elements:
   * **Reconnaissance:** This step represents the research, the identification and the selection of targets.
   * **Weaponization:** It is the coupling between a remote access with an exploit into a deliverable payload. Nowadays, clients' application such as PDF or Word documents are used as a weaponized deliverable.
   * **Delivery:** To transmit the weapon to the target, email attachments, web sites and USB sticks are often used.
   * **Exploitation:** When the weapon is delivered to the target, the weapon can use some vulnerabilities from the OS (automatic execution of code, for example), applications, or the users directly.
   * **Installation:** This step concerns the installation of a backdoor or a trojan inside the victim system. It creates a persistent access for the aggressors.
   * **Command and Control (C2):** Compromised hosts send signals to an Internet control server to establish a C2 channel, which is typically set up manually rather than automatically by APT malware. Once established, the C2 channel allows intruders to have direct access within the target environment.
   * **Actions on Objectives:** It is only in this step that the intruders (aggressors) can take actions to achieve their objectives. Generally, the main objective is data exfiltration (collecting, encrypting, and extracting) from the victim environment.


## 3.3 Courses of Action
The intrusion kill chain is a useful model for defenders to understand and counter the specific processes an attacker uses to target an enterprise. By aligning defensive capabilities with the kill chain, defenders can measure their effectiveness and plan investments to address any gaps. This approach, known as intelligence-driven cyber defense, involves making security decisions and measurements based on a deep understanding of the attacker.

Table 1 is a matrix that shows the different possible actions that the tools (located in the matrix) are able to do. For example, in the operational phase, HIDS is able to detect exploits, patching denies exploitation altogether, and data execution prevention.

<p align="center"> <img width="903" height="577" alt="Table 1: Courses of Action Matrix" src="https://miro.medium.com/max/903/1*7q_uh4DLZ5b62i_e8jfTxA.jpeg"> </p>

* Completeness in security is important because it equates to resiliency, which is the defender's primary goal when faced with persistent adversaries that continually adapt their operations over time.
* Protection against previously undisclosed "zero-day" exploits is important, but it is not the only focus.
* A defensive strategy of complete indicator utilization is key to achieving resiliency against persistent adversaries.
* This strategy involves focusing on repeated indicators and tools used by the adversary, which increases the cost of executing successful intrusions for the adversary.
* This forces of the adversary to make more difficult and comprehensive adjustments to achieve their objectives.

* By measuring the performance and the efficiency of the defensive actions, defenders can create some metrics of the resiliency.
* From the illustration, it is easy to see that one of the mitigation measures has worked. Defenders can protect their infrastructure with this detection. However, a few months later, attackers would try the same flaw again but with more advanced techniques. As a result, they manage to get through again. It is only after the defenders have updated their measures that they are able to defend themselves again.
<p align="center"> <img alt="Figure 2: Illustration of the relative effectiveness of defenses against subsequent intrusion attempts" src="https://github.com/MatthieuBruh/h1_FirstSteps/blob/main/fig2.png"> </p>

------

### [Karvinen 2020: Command Line Basics Revisited](https://terokarvinen.com/2020/command-line-basics-revisited/)
* One of the oldest thing in IT is on the command line. It has been used for a long time, and it has several advantages, like the speed, possibility of automation and it is expressive.
* All the following commands start with a $. You don't have to write it when you write your command.
* When you are writing a command, you can find two signs that you must know:
 * After the $ sign, it is the normal command. It will be executed by the machine.
 * After the # sign, it is a comment. By this fact, you can write what you want, the computer will not execute it.


    $ pwd # This second part is ignored.
    /home/haaga

#### The most used commands in Linux
**MOVING & EXPLORING***

    $ ls # To list all the files of the current directory
    $ cd myDirectory/ # To move into the directory named myDirectory
    $ less helia.txt # Shows the file but page by page (space for next page, b for previous page, slashes for search, q for exist
    $ ls /etc|less # The output of any command can be read a whole screen at a time by sending the output to less

**FILE & DIRECTORY MANIPULATION**

    $ nano foo.txt # Create a text file named foo
    $ mkdir apple # Create a directory named apple
    $ mv OLDNAME NEWNAME # Change the name of a directory
    $ mv fruits home/ # Move the file to the directory home
    $ cp -r first second # Create a recursive copy of a file or directory.
    $ rmdir apple # Delete the directory named apple
    $ rm foo.txt # Remove the foo.txt file

**SSH** <br />
SSH is used to control a machine remotely.

    $ ssh 192.168.1.10 # We connect remotely to the computer that has the IP address
    192.168.1.10$ exit # To close the connection
    $ scp -r FOLDER 192.168.1.10:public_html/ # Copy a file securely to the remoted computer

**HELP**

    $ man ls # To show the manual page of command
    $ ls --help # To show the manual page of the ls command

**HISTORY & GUESSING** <br />
I advise you to use [tab] when you are writing a command. By using it, you will have an autocomplete.

    $ history # Shows you the history of your commands

**DIRECTORY**
| Directory | Explanation |
| --------- | ----------- |
| /         | It is the root directory. |
| /home/    | It is the home directory for all users. |
| /home/jack/ | It is the home directory of the user Jack. |
| /etc/     | Contains all the system wide settings. |
| /media/   | Removable media such an external SSD or a USB stick. |
| /var/log  | Where all the logs of the different packages are stored. |

**ADMINISTRATIVE COMMANDS** <br />
When you are using Linux, I advise you to use the concept of the least privilege. Avoid as much as possible to be as an administrator with the 'sudo' command.

    $ sudo apt-get update # Update a list of available packages.
    $ apt-cache search dungeon adventure # Search for software with keywords, NO SUDO NEEDED
    $ sudo apt-get install apache2 # Install the package apache2
    $ nethack # To run nethack
    $ sudo apt-get purge nethack # To remove the package nethack


------

<a name="solve"></a>
# Solve
### [Bandit oh-five](https://overthewire.org/wargames/bandit/)

## Level 0
To ssh bandit.labs.overthewire.org on the port 2220 with the username 'bandit0'. We have to use the *-p* to choose a specific port

    $ ssh bandit0@bandit.labs.overthewire.org -p 2220

## Level 0 -> 1
My first reflex was to check the file in my current directory. Of this fact, I use the following command:

    $ ls

I saw that there was a file named 'readme'. I decided to open it to see the content.

    $ cat readme

With the previous command, I was able to read the password that was hidden in the file. So, I copied the password. Then, I closed the connection with the command <code>exit</code>. Now, I am able to connect to the server with the new username and password. I used the same command as the level0, but I changed the username.

    $ ssh bandit1@bandit.labs.overthewire.org -p 2220

## Level 1 -> 2
I have to search a file in the home repository. So, I decided to go back in the file tree. By using the command:

    $ cd ..

Now, I knew that I have to find a file called -. So, to find and open a file in the same time, I wrote the command:

    cat `find /home/ -name "-"`

## Level 2 -> 3
This level was not really complicated. When I found the document, I just started to write the name of the file and I used [tab]. It gives me this command:

    cat spaces\ in\ this\ filename

## Level 3 -> 4
For this level, I used the ls command and the option that are available. So, I added the option *-a* to see all files and directories.
I found a file and I opened it, there was the new password.

## Level 4 -> 5
Firstly, I moved to the inhere directory. Then, I have to find a file that contains some ASCII characters. So, I decided to try the command:

    file ./-file*

Then, I knew which file was containing some ASCII characters. By this fact, I decided to cat the correct file to find the password.




------

<a name="warmup"></a>
# Hacker warmup
### [WebGoat](https://owasp.org/www-project-webgoat/#:~:text=WebGoat%20is%20a%20deliberately%20insecure,and%20popular%20open%20source%20components.)

## General: HTTP Basics

## General: Developer tools
