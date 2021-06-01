## README file for Chapter 1 : Working with Shell

#### 1_A) Introduction to Shell :

    - The Linux shell is a program that allows text-based interaction between the user and the OS using commands.
    - Command syntax : `command <options> <arguments>`
    - <options> (AKA switch or flag) is usually a single letter preceded by a single "-". They are used to modify the command behaviour in some pre-defined way.
    - Command Types :
        a) Internal or built-in commands
            - These are part of the shell itself.
            - Approx. 30 commands
            - Eg. cd, echo, pwd, mkdir, set etc.
        b) External commands
            - These are binary programs or scripts which are usually located in distinct files in the system.
            - They either come pre-installed with the distributions package manager or can be created and installed by the user.
            - Eg. mv, date, uptime, cp etc.
    
    - Commands :
        | S.No. | command | Description | Example |
        | :------| :------| :------| :------|
        | 1 | echo | To print a line of text on the screen | $ echo -n Hello |
        | 2 | uptime | To print information about how long the system has been running for since the last reboot. | $ uptime |
        | 3 | type | To determine if a command is internal or external | $ type echo, type mv |

#### 1_B) Basic Linux Commands :

    - 