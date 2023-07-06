# BootCon Final Project - Ghidra Demonstration

## Project Summary
In this project, I utilized Ghidra, a software reverse engineering tool developed by the NSA, to reverse engineer a program. The 'crack me' file was downloaded from crackmes.one, a platform that hosts various 'crack me' files written in different languages for different platforms. The objective was to discover the correct password for the program.

## Downloading and Setting Up Ghidra
The initial step involved downloading Ghidra from its GitHub page. After downloading the zip file from the releases folder, I extracted it and initiated the program by running the batch file. Subsequently, I created a new project within Ghidra and assigned it a name.

## Analyzing the 'Crack Me' File
I imported the 'crack me' file into Ghidra by dragging and dropping it into the program via the code browser. Ghidra then prompted me to analyze the file, to which I agreed. I adjusted a few analysis settings, such as unchecking the pdb Universal (which tends to cause errors) and checking the windows PE x86 parameter.

## Finding the Password
Upon the completion of Ghidra's analysis, I searched for the string "nope, that's not it", which was the response given when an incorrect password was entered into the 'crack me' program. I found references to this string in the code and examined the function where it was used.

In the decompiled code, I noticed an if statement where a specific data value was being stored in a function called 'm-e-m-cmp'. This value had to match the data value for the program to output "congrats, you got the password right". I then looked at where this data value was written to find the correct password.

## Conclusion
By examining the decompiled code and understanding how the program checked for the correct password, I was able to find the correct password and successfully reverse engineer the program. This project showcased my ability to use Ghidra for software reverse engineering.

## Tools Used
- Ghidra: A software reverse engineering tool developed by the NSA.
- Crackmes.one: A platform hosting 'crack me' files for reverse engineering practice.

## Video Demonstration
For a detailed walkthrough of this project, you can watch the [video demonstration](https://youtu.be/5I3TOtLiP04) on YouTube.
