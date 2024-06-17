# Accessing the System
## Remote System Access

- To access Super Computing Facility of Tribhuvan University you need to “ssh” the login server.

- The login node is primary gateway to the rest of the cluster, which has a job scheduler (called Slurm). You may submit jobs to the queue and they will run when the required resources are available.

- Please do not run programs directly on login node. Login node is use to submit jobs, transfer data and to compile source code. (If your compilation takes more than a few minutes, you should submit the compilation job into the queue to be run on the cluster.)

- Under your /home/user directory there is a storage0 or simialar. Use this folder to hold the store the data required for runnung the job.

### Remote access from Windows Desktop
[PuTTY](http://www.putty.org/) is the most popular open source “ssh” client application for Windows, you can [Download it from here!](https://www.chiark.greenend.org.uk/~sgtatham/putty/). Once installed, find the PuTTY application shortcut in your Start Menu, desktop. On clicking the PuTTY icon The PuTTY Configuration dialog should appear. Locate the “Host Name or IP Address” input Field in the PuTTY Configuration screen. Enter the user name along with IP address or Hostname with which you wish to connect.

(e.g. [username]@hpc.tu.edu.np)

Note: remove the '[    ]' from username.

Enter your password when prompted, and press Enter.

### Remote access from Linux Desktop / Mac

Both Mac and Linux systems provide a built-in SSH client, so there is no need to install any additional package. Open the terminal, connect to an SSH server by typing the following command: 

```ssh -X [username]@[hostname]``` 

For example, to connect to the Super Computing Facility of Tribhuvan University Login Node, with the username

```user: ssh -X user1@hpc.tu.edu.np```

You will be prompted for a password, and then will be connected to the server.


## First login

- Whenever the newly created user on Super Computing Facility of Tribhuvan University, tries to login with the user Id and password (temporary, system generated) provided over the Email through ICTC support, he/she should change the to new password.

Given next is a screenshot that describes the scenario for “first login”
![image](/assets/img/fingerprint-login.png)

Type : yes, otherwise the system will disconnet.

- It is strongly recommended to change password after first login.

## Change Password
- It is recommended that you have a strong password which contains the combination of alphabets (lower case / upper case), numbers, and a few special characters that you can easily remember.

- To change the password, Use the ```passwd``` command to change the password for the user from login node.

![image](/assets/img/change-password.png)

Note: The typed password is invisible in terminal.

## Forgot Password?

Please raise a ticket regarding this issue under  User Support  and the system administrator will resolve your problem. 


