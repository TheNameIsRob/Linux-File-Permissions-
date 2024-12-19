
<h1>Linux Exercises: Files and Directories</h1>

<p>This tutorial demonstrates how to utilize different commands to grant and restrict user permissions for files and directories</p>

<center>
<img src="https://i.imgur.com/10h3rUd.png" width="500" height="400"> 
</center>

<h2>Environments and Technologies Used</h2>

- Oracle VM Virtual Box
- UBuntu Linux
- Linux Shell

<h2>Task 1: Check File and Directory details</h2>
<p>By using the  ls -la command , we are given the opportunity to view all directories and files including the ones that are hidden. This displays the users permissions for each file and directory.</p>
<img src="https://i.imgur.com/AbfFpOp.png")>
<p>By observing this screenshot of the command line, we see that the first block displays a series of different permissions.</p>

<h2>Task 2:  Describe the permission strings and change file permissions</h2>
<p>As we see in the first block, there is a string of 10 letters that represent different things for the 5 files. Firstly, the first letter represents a directory which is represented by the letter “d” or for a file it is represented by a hyphen “-”. The remaining 9 letters will contain the letters “r” “w” and “x” which will represent whether a user has read,write and executable privileges. Each 3 letters are divided into different owner permissions which are the user,group and others (others in the system)</p>
<p>The organization requires that write permissions should not accessible to other as we see below. In order to change this permission we need to use a specific command remove the access of this permission in this file.</p>
<img src="https://i.imgur.com/1n4LnTk.png">
<p>In this case we will use chmod with the following texts o-w project_k.txt to specifically target the other section of this file to remove its write permission. On the command line it should look like this. chmod o-w project_k.txt</p>
<img src="https://i.imgur.com/FZpN7Q7.png">
<p>Now we can see the simple difference between the 10 letter string. The last 3 letters represent other, and no longer contain the letter “w” which lets us know that this permission has been removed.</p>

<h3>Task 3: Change the permissions on a hidden file</h3>
<p>The research team has archived the file .project_x.txt (a  period “.” before the file name means it is a hidden file). </p>
<img src="https://i.imgur.com/dJkje9g.png">
<p>This specific file should not have write permissions for anyone, but user and group should be able to read the file. We will use chmod u-w,g-w .project_x.txt to remove write privileges for user and group and add chmod g-r .project_x.txt  to give the group the read permission.
</p>
<img src="https://i.imgur.com/6vSjqZz.png">
<p>Again we see that a simple change has been made. Write privileges have been removed for user,group and other but we see user and group have read permissions represented by the letter “r”. These are the correct permissions.</p>

<h3>Final Task: Change directory permissions</h3>
<p>The user by the name “Researcher2” as shown on the command line should be the only user with executable privileges for the drafts directory. Again by observing the command line we see that this is not the case </p>
 <img src="https://i.imgur.com/Yjaj9DU.png">
 <p>We will use chmod g-x drafts to fully remove the executable task in group represented by the letter “x”.
</p>
<img src="https://i.imgur.com/xiKNZwU.png">
<p>Now we see that group no longer has the executable permission and the user is the only one with this privilege. 
</p>

<h3>Summary
	By using the Linux command line, we were able to view files and directories that contained specific permissions. It is important to make sure that certain privileges are authorized or restricted to maintain a secure system. Performing these tasks by the use of commands will always be valuable in making sure an organization keeps good security posture. 
</h3>
