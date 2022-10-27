# Jmeter-Perfornamce-Practice
JMETER

Test Fragment is like background.. "login"

Download Jmeter and eecute it from bin --> jmeter.bat file with double click
To Create First TC
Test plan -> RC -> Thred Group -> Add --> Sampler --> RC -> HTTP Request
Thred Group -> RC -> Add --> Listener --> View Results Tree
Thred Group -> RC -> Add --> Listener -->  View Results in Table
Thred Group -> RC -> Add --> Listener -->  Aggregate Report
Thred Group -> RC -> Add --> Listener -->Simple Data Writer  , create a file on desktop or so , report.csv
and open it from Simple Data Writer filename path


Assertions
Assertions =  checks on the Request/Response
we can add Assertion in Test Plan level
Thread Group Level or  else level.. Test Plan level will implimented all level
1 Response Assertion
Test Plan --> RC--> Add -> Assertion
we can also add Listener --> Assertion Results to see all assertion results


2 Duration Assertion
3 Size Assertion
4 HTML Assertion
5 XML JSON Assertion
6 XPATH Assertion

JMeter HTTP(s) Test Script Recorder
What
Why
When
How

How to record your test on JMeter
Test Plan --> RC --> add --> Non-Test elements --> HTTPs Test Script Recorder
Add --> Thread Group --> RC --> add --> Logic Controller --> Recording controler
time stamp : 1:00

How to add & use Test Script Recorder
How to add & use Recording Controller
How to use proxy on Firefox, Chrome and System
How to add SSL Certificate
How to do Request Filtering
How to use Recording Template


COMMAND LINE EXECUTION

Windows

Go to Jmeter --> bin and Open in CMD
type -- > jmeter -n -t "C:\apache-jmeter-5.3\JmeterEvidential\EVGetObject"\SupplierJM.jmx -l "ReportTest12.csv"
jmeter -n -t “location of your test file” -l “location of results file”

to execute Test Cases from Command line any location -- >
Add path including bin  to  environment variables Path

C:\Users\nyilmaz\Desktop\apache-jmeter-5.5\bin

C:\Users\nyilmaz>jmeter -n -t "C:\Users\nyilmaz\Desktop\SampleFiles\fileUploadTest.jmx" -l "C:\Users\nyilmaz\Desktop\result.csv" -e -o "C:\Users\nyilmaz\Desktop\reportHtml"

Location of Test file :C:\Users\nyilmaz\Desktop\SampleFiles\fileUploadTest.jmx"
Location of CSV file  where we want to create : "C:\Users\nyilmaz\Desktop\result.csv"
Location of HTML REport  where we want to create : C:\Users\nyilmaz\Desktop\reportHtml"

CREATING A REPORT FROM EXISTING RESULT

C:\Users\nyilmaz>jmeter -g "C:\Users\nyilmaz\Desktop\result.csv"  -o "C:\Users\nyilmaz\Desktop\report123"

TO SEE THE GRAPH WELL GO TO BIN --> REPORTGENERATOR.PROPERTIES FILES AND CHANGE GRANULATY TO 2-3 SECS , BY DEFAULT IT 60 SECS


FILE DOWNLOAD
https://www.youtube.com/watch?v=Tzqd1xSPc3s&list=PLhW3qG5bs-L-zox1h3eIL7CZh5zJmci4c&index=28

PLUGINS
download jar file . go to jmeter folder open lib --> EXT folder and add  jar file to it
jmeter plugins manager to add all plugins on jmeter ui
NOTES

PIPELINE JENKINS  
https://www.youtube.com/watch?v=mYGQPj78YhI&list=PLhW3qG5bs-L-PpK83CC_m_bWd_722tvgk&index=1&t=28s

JMeter + Jenkins

Step 1 : Install Jenkins
(https://www.youtube.com/watch?v=89yWX...)

Step 2 : Get Jenkins Performance Plugin
(https://wiki.jenkins-ci.org/display/J...)

performance.hpi file - put into Jenkins - Plugins folder
Restart Jenkins

You can also install this plugin form Jenkins - Plugin Manager.

Step 3 : Goto Jmeter/bin
user.properties - add line :
jmeter.save.saveservice.output_format=xml

Step 4 : Create a Jmeter test

Step 5 : Run JMeter test from command line

cd /Users/raghav/Desktop/Tools/apache-jmeter-3.0/bin/
sh jmeter.sh -Jjmeter.save.saveservice.output_format=xml -n -t /Users/raghav/Desktop/JmeterJenkinsIntegrationTest.jmx -l /Users/raghav/Desktop/TestResult1.jtl

Step 6 : Add a job in Jenkins - add jmeter commands in build step

Step 7 : Add post build action - publish performance test reports

Step 8 : Run and validate


What is JMeter

Performance test application
Build using Java
Free & Open Source
Recording
CLI
Reports

How to install JMeter
Windows | Mac | Linux

1 Check java is installed on your system
java -version
2 Download JMeter    
3 Unzip and keep Jmeter folder at any locatio
4 Start JMeter
Windows - jmeter/bin - jmeter.bat        
| Mac - open terminal - jmeter/bin - sh jmeter.sh

JMeter GUI Overview

How to create first Jmeter Test

1 Start JMeter
2 Create a TestPlan
3 Create a Thread Group (Users)
4 Add a Sampler (Http)
5 Add Listeners
6 Run the Test

JMeter Listeners (Reporting)
Used for Reporting

listener = elements that gather information about the performance test
used to view results/metrics of the test

Latency = time to first byte

0ms—————————1000ms—————————2000ms
0ms —————————————————————— 2000 ms

1 View Results in Table
2 View Results Tree
3 Aggregate Report
4 Graph Results
5 Summary Report
6 Simple Data Writer

Assertions
Assertions =  checks on the Request/Response

1 Response Assertion
2 Duration Assertion
3 Size Assertion
4 HTML Assertion
5 XML JSON Assertion
6 XPATH Assertion

JMeter HTTP(s) Test Script Recorder
What
Why
When
How

How to record your test on JMeter
How to add & use Test Script Recorder
How to add & use Recording Controller
How to use proxy on Firefox, Chrome and System
How to add SSL Certificate
How to do Request Filtering
How to use Recording Template

How to use Blazemeter to Record JMeter Tests

1 Create Blazemeter Account
2 Get Blazemeter Extension
3 Login to Blazemeter
4 Record test
5 Save JMX
6 Add JMX in JMeter and Run

JMeter - How to get data from CSV File
Config Element - CSV Data Set Config

1 Add CSV Data Set Config
2 Create a csv file and add data
3 Refer the csv file in JMeter’s csv data set config
4 Refer values from csv file using syntax ${variableName}
5 Run and validate

JMeter Config Elements - for HTTP (Web Test Plan)
Elements that are executed before the sampler requests at the same level
Configuration elements can be used to set up defaults and variables for later use by samplers. Note that these elements are processed at the start of the scope in which they are found, i.e. before any samplers in the same scope

Demo app - https://opensource-demo.orangehrmlive...

How to run JMeter from command line
GUI consumes memory, slower
integrate with any external process CI CD

How to run JMeter test from command line
How to log results
How to see command line help and options
How to run from any location on your system (add in Path env variables)

Step 1 - Open Command line ＞ Goto JMeter’s bin folder
Run command

Windows
jmeter -n -t “location of your test file” -l “location of results file”

Linux / Mac
sh jmeter -n -t “location of your test file” -l “location of results file”

How to extend JMeter | JMeter Plugins Manager

Easy & Quick way to:
Find plugins
Install
Uninstall
Upgrade

Plugins - https://jmeter-plugins.org/wiki/Start/

1: Download plugins manager jar from https://jmeter-plugins.org/wiki/Plugi...
2: Add the jar file in jmeter lib/ext folder and restart JMeter
3: Check JMeter plugins manager is added

Functions & Variables
What are functions
What are variables
How to use functions and variables

Functions - methods used to populate fields in any other element of test plan

Syntax
${__funcName}
${__funcName(var1, var2, ….)}

Variables - containers that can store values, which can be referred in any element within a thread
${varName}

