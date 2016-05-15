# Project_Information
The readme file about the whole project

readme version: 1.0    2016-05-15

------------------------------------------------------------------------------------------------------
Index:

1. Introduction
2. Ideas
3. Security Controls
4. Code writing style and standards
5. Project Parts



------------------------------------------------------------------------------------------------------

1. Introduction

as programmers we use APIs (Application Programming Interface) for different things from showing a windows message to interacting with facebook servers.

on the other side there are programmers who make these APIs, the facebook team making an API to let us connect and build thirdparty applications, tweeter
team making APIs to let us connect to their site and get tweets of people and ....

So.... if you are an API developer or would like to write an API for your site, you need to test this API on heavy load, when thousends of applications will send
requests to your API, Imagine the tweeter API responsing to millions of requests every hour

the problem is for the heavy testing of an internet based API server, we need millions of user computers to send requests ! that almost imposiblle to achive, 
therefore companies with a lot of investment buy thousands of computers and run multiple virtual servers on them to simulate the real situations for the test,
this is really EXPENSIVE, also there are companies who are specially do heavy load testing for very high prices (say 20,000$ for one test)

Now we have the problem:  API LOAD TESTING IS VERY EXPENSIVE due to the cost of the job

so What:  We have and idea of using the services of "GOOGLE CLOUD COMPUTING ENGINE" , its fast, powerfull and cheap

****  The Whole system is based on NodeJS, and the user will write the test scripts in Javascript language for NodeJS   ****

------------------------------------------------------------------------------------------------------

2. Ideas

The Idea is to use services of "GOOGLE CLOUD COMPUTING ENGINE"

Google provides millions of Virtual PCs with CPU and Memory of your choice in a click of a button all over the world with high speed internet connection, 
The billing of these services are based on the Virtual-PC type we choose and the time of operation run per minute, and its really really CHEAP

So what we need to do is Make an application witch will connect to Google services and request a number of VPCs (let say 10,000) created with our settings, 
then run the Test script on them by building inner virtual users (let say 1000 virtual users), Now we have a 10,000,000 user Test operation


Thats the Idea.....

------------------------------------------------------------------------------------------------------

3. Security Controls

Because it will be a cheap service, there is a possibility of missuse by hackers for ddos and other types of attacks, so to prevent these we need to make some 
limitations on users scripts, like NO fs, NO Socket, NO .... etc

also we need some messures to prevent user script from harming the Main application process


------------------------------------------------------------------------------------------------------

4. Code writing style and standards

Will complete this part later, for now use hapi.js style (i use it with a few changes to match my taste)

I will be using Hapi.js Code writing style, make sure to read the style guide before you write any code for us (http://www.hapijs.com/styleguide)


------------------------------------------------------------------------------------------------------

5. Project Parts

a. virtuall user engine (VUE), witch will run the Test_script

b. Virtual machine Engine (VME), this will run lots of VUEs on one machine

c. Analysis Engine (AE), this will do the analysis on the gathered data

d. Data capture middleware, it will put to work on every VUE to gather the data required for AE

e. Load Test Engine, this will join the parts and connect to Google services and start the work

f. Extra parts like Accounting middleware, official Site , documantation and etc.


------------------------------------------------------------------------------------------------------

as project moves forward, this text file will be updated

Regards
Hassan Eslaminezhad