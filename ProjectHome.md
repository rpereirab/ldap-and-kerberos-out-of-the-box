LDAP and Kerberos out-of-the-Box for Ubuntu Linux

Code written by Patrick Clancy
README Written by Patrick Clancy
Project proposed by Patrick Clancy
Contact Info: patrick.j.clancy@gmail.com

Mentored by Rodrigo Pereira Braga (pereira@gmail.com)

Google Summer of Code 2007

Table of Contents

I.	Overview
II.	Tool Information and Dependencies
III. 	Running the Code
IV.	Editing the Code
V.	Future Work


I. Overview

This project is the result of two other projects that were canceled
during the summer of 2007.  Initially, we had planned to write a
program to install the Fedora Directory Server, but after weeks of
work with little success, we realized that FDS may not be a viable
option for Ubuntu.

After the FDS problems, we needed to change the direction of the
project.  The minimum goal was automating the installation of a
simple LDAP server.  So the first steps were figuring out how to
install LDAP on Ubuntu.  After that we needed to find out what
pieces of information were needed for the LDAP installation. Around
this point we found out that work had resumed on the another Ubuntu
project that did all of this work already. The program was called
authtool, and it supported a number of different authentication
protocols.  Among them was an LDAP and Kerberos server.  After
seeing the code for the backend, it was clear that it would take
us more than a month to improve upon the installation, but the
frontend was not nearly as well established.

So, the final project was working on the authtool frontend for
LDAP and Kerberos, because the only information given was the title
of each text entry box.  I added a regular expression syntax checks
and information buttons that explained the purpose of each piece of
information.  These features should make deploying a LDAP+Kerberos
server significantly easier.



II.	Tool Information and Dependencies

I wrote the programs using the Emacs editor, designed the GUI with
the Python Glade-2 GUI builder, and used Python code to tie
everything together.  If you want to edit the code, install the
following Ubuntu Packages:
> python
> glade-2
> emacs




III. 	Running the Code

Once you have the necessary dependencies installed, you can enter
the appropriate directory and run the code with the following
command:

> python LDAP\_and\_Kerberos.py

From here use the program as instructed, check the syntax of your
entries by clicking the button labeled "More Info" next to the
text entry box.


IV. 	Editing the Code

To edit the code use your favorite text editor to LDAP\_and\_Kerberos.py,
and use glade-2 to edit LDAP\_and\_Kerberos.glade.  Be sure to build
the GUI using glade-2's built-in "Build" function.


V. Future Work

There are a number of reasons why I would like to continue this
work after the Google Summer of Code.  First of all, my project
changed three times, so I didn't get as much time to work on it
as I would of liked.  Second, I see that I can help improve code
for Ubuntu in my free time.  Third, Ubuntu doesn't have a great
tool for easily installing authentication, and authtool would help
Ubuntu take the next step into the server market if it worked well.

So, I would like to continue writing authtool front ends.  The next
step would be writing another tool for a NIS server.  It would build
nicely on the work I have already done.