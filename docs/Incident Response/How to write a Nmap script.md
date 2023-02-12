How to write a Nmap script



In this small guide, we are going to learn some Lua basics and how to write a simple Nmap script. If you are into information security and networking you probably heard of the Nmap scanner. 
In this post, I want to take this opportunity and discuss how to develop Nmap scripts using Lua programming language. According to its official website (https://nmap.org/ ): “Nmap ("Network Mapper") is a free and open source (license) utility for network discovery and security auditing. 
These are some Nmap commands to perform different types of network scanning:

Nmap is a powerful Tool. It can perform other tasks besides network scanning. It is loaded with many useful scripts (.nse) thanks to a Scripting Engine. Discovery and vulnerability detection are some of these tasks. 
To write NSE scripts we need to explore the Lua Programming language first. Let’s have a small glimpse about it. Lua is an open source language built on top of C programming language. It was developed by Roberto Ierusalimschy, Luiz Henrique de Figueiredo, and Waldemar Celes in 1993. It is used in a wide range of applications because it is open, simple and efficient. 
To write Lua programs we just need a text editor and an interpreter. Vim will do the job. Create a new file with .lua extension and you will be ready to go. To download Lua interpreter on Linux type:
wget http://www.lua.org/ftp/lua-5.2.3.tar.gz
Extract it, enter the lua folder and run make linux test
For this demo, I am using a dedicated Azure Machine 


Lua Basics:
To print “Hello World!” type 
print “Hello World!”
And run the script message.lua with lua command lua message
Comments:
--[[ comment Here --]]
Variables: 
Lua is dealing with 3 types of variables: Global, Local and table fields. They are defined as the following;  type Variables; for example:
Local X, Y; 
X=1
Y=2
print (“variable X: ”,X)
Variable types: 
Lua is dealing with 8 types: 
Nil
Boolean
Number 
String
Function
Userdata
Thread
Table
To explore them in details check the TutorialPoint resource in the references section
For logical operations and escape symbols they are the same as the other languages i guess (and, or, \" and so on)
Now let’s have an overview of how to write an Nmap script. A typical nse script is respecting the following format:
HEAD: meta information about the script
RULE: It is a Lua method to decide when you run the script based on rules
ACTION: the functionality of the script 
For the HEAD you can add a description section
description = [[
This is a Lua script to perform ...
]]
You can add other tags like: author, licence and category. 
author = "Author name here"
In this section you need to add the imported libraries for example:
local nmap = require "nmap"
To explore a nse script sample check this small script: https://github.com/petermbenjamin/nmap-nse-scripts/blob/master/rails-admins.nse
To learn more about NSE scripting you can read the official Nmap online book: https://nmap.org/book/nse.html
References
https://www.tutorialspoint.com/lua/lua_arrays.htm
https://nmap.org/book/nse-tutorial.html
https://media.blackhat.com/bh-us-10/whitepapers/Vaskovitch/BlackHat-USA-2010-Fyodor-Fifield-NMAP-Scripting-Engine-wp.pdf
https://medium.com/@pmbenjamin/writing-nmap-scripts-like-a-super-hero-e4b0dc4c782
http://thesprawl.org/research/writing-nse-scripts-for-vulnerability-scanning/


