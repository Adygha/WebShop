# Test Strategy

### 1 Introduction

##### 1.1 Definitions and Acronyms

* __Assignment-2__: Is the testing project name that this, and any following, document is going to cover.
* __SDC__: Stand for 'Software Development Company,' which is the software company that requested the testing.
* __IoT__: Stands for 'Internet of Things,' which is a notion in which everyday objects can be sensed and/or controlled remotely across a network.
* __My Web Server__: An open source abandonware software that is a candidate for being the basis of an IoT. This software is the system to be tested as requested by SDC.
* __SUT__: Stands for 'System Under Test.' It represents the system requested to be tested in Assignment-2. Check 'My Web Server' up.
* __Test-Lord__: Is the single SDC emploee (the student doing this assignment) that Assignment-2 project is assigned to.
* __Stakeholders__: All the parties interested in the test results of the Assignment-2 project. In our case we will assume Assignment-2 as a real life project (and not as an assignment); thus, the stakehoders in our case will be SDC (future IOT-developers and end-customers are not of our concern now.)
* __Requirements__: The requirements document provided by SDC that SUT will be checked against.
* __Phase-#__: To organize the work on Assignment-2, the working hours on Assignment-2 are divided into 5 phases with 8 hours for every phase (Phase-1, Phase-2, etc...)

##### 1.2 Overview And Purpose
This document represents the broad strokes of the manual testing approach that is going to be excuted in relation to 'Assignment-2' of the '2DV610 Software Testing' course to evaluate the current state of SUT and whether it fulfills the requirements provided by SDC (the requirements will be presented in the test-plan document in detail). This test strategy is done by the 'Test-Lord', and will also be the starting point in developing the test plan, which is done by 'Test-Lord' too. Although it is not likely; this document, or part of it, is maybe subject to a slight change as the project progresses.

##### 1.3 Testing Objectives
Assignment-2 objectives are summarized in the following points:
* Evaluate the current state of SUT.
* Check if SUT fulfills UC1, UC2, and UC3 use cases mentioned in the Requirements document.
* Check if SUT fulfills the supplementary specification requirements mentioned in the Requirements document.

##### 1.4 Scope
Due to resource limitations (resources covered in a later chapter,) some parts will be out of the scope of this test.

###### 1.4.1 In The Scope Of This Test
Assignment-2 will only cover testing the use cases provided in the Requirements and its supplementary specification section.

###### 1.4.1 Out Of The Scope Of This Test
This test will not cover the requirements outside the Requirements document provided by SDC (e.g. 'minimal configuration as well as easy integration' that maybe requested by future expected IoT-developers). Testing will not check if SUT works on Mac operating system due to the lack of hardware resources. Additionally, checking if SUT works on Linux will only be covered if the time, as a resource, permits (which can be decided in the test plan.) Since SUT is provided as a working system, static qualities testing will not be covered in Assignment-2, and only dynamic qualities testing will be covered.

### 2 Resources
This chapter will discuss the resources for Assignment-2.

##### 2.1 People And Their Time
Assignment-2 will have only one person (Test-Lord) to handle all the activities related to Assignment-2. The time assigned according to this personnel limitation is one man-week (40 hours.)

##### 2.2 Hardware And Software
For running the test there is one laptop available. This laptop has Windows 10 and Linux Mint 18 operating systems installed, but due to time limitation it is suggested that all the testing take place in the Windows environment first and then on the Linux environment if the time permits (the test plan will decide.) If the time in the test plan permits, we can use 'JMeter server performance testing tool' against SUT. 'Firefox' web browser will be used as a main client for testing SUT on the same machine that runs SUT. Additionally, windows 'telnet' client command will be used to send some specific HTTP1.1 requests (telnet also suns on the same machine that runs SUT).

### 3 Testing Approach And Organization
To cover the test type, the testing for this project will use the manual *system* testing to achieve testing objectives. The testing process will be divided into test cases that will be linked back to every scenario in the use cases and/or to a non-functional requitement in the Requirements document (the linking will be achieved by using a table.) The following sub-chapters will cover the other approach aspects.

##### 3.1 Test Cases' Priority And Severity (Classification)
In this sub-section we will classify the test cases' priority and severity of a test case so that we can prioritize the testing process, and give an estimate in final report of how severe a failed test will impact the final decision of adopting the SUT (So, in our case, the severity will decide and have the same classification as priority.) The classification will be:
* Low: To specify that a test case has a low priority for testing in a testing phase and can be postponed for a while if the time dos not permit. Additionally, 'low' means that a test case has a low impact on failing of a scenario and/or a non-functional requirement.
* High: To specify that a test case has a high priority for testing in a testing phase, and that a test case has a high impact on failing of a scenario and/or a non-functional requirement.
* Critical: If test case is marked as critical, all the scenarios and/or the non-functional requirements that can be traced back to it will be considered as totally 'Not-Achieved' (this classification can mark a whole use case as 'Not-Achieved' if it affects a main scenario of a use case). This classification is added in the final stages of the strategy document to be used just in case there is a test case that needs it (and it might not be used.)

##### 3.2 Pass/Fail Criteria
Test cases will be created based on scenarios of use cases and/or non-functional requirements that we can find in the Requirements document provided by the stakeholders which in our case is SDC (please check 'stakeholders' in '1.1 Definitions and Acronyms' sub-section). Those test cases will have steps that can be followed to conduct the particular test case. In addition to steps, every test case has expected results and and actual results, and if they do not match, the status for the test case will be marked as a 'Defect' first until the the phase ends where we check if the test case needs to be altered or the test case should be marked with 'Fail' as a status. A test case can have 'Partially-Success' status if it depends on another 'Low' priority/severity test case. A failed test case can mark every scenario and/or non-functional requirement that can be traced back to it as 'Not-Achieved' (or maybe 'Partially-Achieved' depending on its severity (please check previous sub-chapter.)

##### 3.3 Testing Phases And Milestones
In this document it is suggested that the testing process be divided to phases with 8 hours for every phase. Since the time resource is 40 hours worth of work, and reading about and preparing this test strategy document seem to take roughly 8 hours, we will consider working on this test strategy as Phese-1. The other phases will be decided in the test plan document, but as a preliminary assesment, Phase-2 will be for working on the test plan. Every phase will be concluded with an accomplishment which is the milestone for that phase. So, for Phase-1 the milestone is the completion of this test strategy document, and Phase-2 will have the completion of the test plan as its milestone (other milestones will be decided in the test plan document).

##### 3.4 Roles And Responsibilities
Test-Lord will be responsible, in addition to creating this test strategy, of creating the test plan, preparing the test cases, conducting the actual test according to test cases, and writing a test report.

##### 3.5 Risk Management
The main risk management strategy considered in Assignment-2 is by providing a backup of the physical resources (in our case it is just the laptop where a plan to borrow one from a friend is prepared). Additionally, a simple, but efficient file backup plan was also prepared using an online storage space. As for the time consuming risks, a solve-on-the-spot approach is considered (since it is a one-man-team.)


---
# Test Plan
__Note__: please check '1.1 Definitions and Acronyms' sub-section in the test strategy document for any definition or acronym that might appear in this document.

---
# Test Cases
__Note__: please check '1.1 Definitions and Acronyms' sub-section in the test strategy document for any definition or acronym that might appear in this document.

In this test cases document, all the test cases are designed in Phase-3 and executed in Phase-4. Additionally, all the test cases are designed and executed by Test-Lord (this was stated here to avoid the repetition in every test case.) All the test cases are conducted on the SUT as a jar file named 'SUT.jar' and run in a comman prompt using the command 'java -jar SUT.jar'. When 'Standard-Parameters' is mentioned in the test data, that means the SUT will be run with the parameters '`8099`' for port number, and the path '`C:\TestField\inner`' in case of Windows OS or '`@HOME/TestField/inner`' in case of Linux OS as a path for the working resource container for SUT (the content of 'TestField' folder ar extracted from the resource folder of SUT's source code.) The parameters for port and path may change if the test specifies that in the test data.

### Test Case TC-1 : Existence Of Logging System
|Test ID|TC-1|
|---|---|
|Test Name|Existence Of Logging System|
|Test Description|A stand-alone test case to make sure that SUT has a logging system that create an access log as a text file that is viewable using a text editor (This test case is solely created to test SUP-5.)|
|Test Data|Standard-Parameters. Web-Address = '`http://localhos:8099`'|
|Test Classification (Priority/Severity)|Low|
|Pre-conditions|Make sure that only 'SUT.jar' exists in the current running folder and no residual files exist from a previous run. SUT is not running.|
|Test Steps|1 - Run SUT according to parameters in test data.|
||2 - Access the shared resources using the web browser by visiting the web address in test data.|
||3 - Stop SUT by typing 'stop' in the console and hitting Enter.|
||4 - Check if a 'Log.txt' (or similar) file was created where the 'SUT.jar' file is.|
|Expected Results|A 'Log.txt' (or similar) file, with content viewable using a text editor, is created during the execution of the test steps.|
|Post-conditions|SUT is shut down normally and not in running state.|
|Actual Result|No log file was created|
|Test Status|Fail|

### Test Case TC-2 : Access Log Written (Not Stand-Alone)
|Test ID|TC-2|
|---|---|
|Test Name|Access Log Written (Not Stand-Alone)|
|Test Description|A __non__-stand-alone test case (that is part of other test cases as an expected/actual result) to make sure that SUT has written a note in the access log or not. This test case was created based on the assumption that if no logging system exists, this logging property can be added easily or the need for it can be ignored, and it is better not to mark all the riquirements that depend on it as 'Not-Achieved' if other, more important, aspects are achieved.|
|Test Data|A __note__ from the main test case that is to be written in the access log.|
|Test Classification (Priority/Severity)|Specified by the main test case that this test case is a part of. For example, if the main test case specifies, as an expected result, that a note is diplayed on the console and also written in the access log, then TC-2 can be classified as 'Low', but if the main test case expects only that a note is written in the access log, then TC-2 can be classified as 'High'. To sum-up, this test case always fails but with different severity.|
|Pre-conditions|Another test case (main test case) has TC-2 as an expected result.|
|Test Steps|1 - Perform the main test case.|
||2 - Check if the expected note from the main test case is written in the access log.|
|Expected Results|Expected note from the main test case is written in the access log.|
|Post-conditions|N/A|
|Actual Result|No note is written in any access log.|
|Test Status|Fail|

### Test Case TC-3 : Start SUT With No Parameters
|Test ID|TC-3|
|---|---|
|Test Name|Start SUT With No Parameters|
|Test Description|Makes sure that SUT asks for a port number and shared resources container if it was run without providing them.|
|Test Data|N/A|
|Test Classification (Priority/Severity)|Low|
|Pre-conditions|Make sure that only 'SUT.jar' exists in the current running folder and no residual files exist from a previous run. SUT is not running.|
|Test Steps|1 - Run SUT with no parameters.|
|Expected Results|An error message requiring providing a port number and a path to shared resources container is presented.|
|Post-conditions|SUT exits.|
|Actual Result|An error message requiring providing arguments (for port number and path to shared resources container) when running SUT.|
|Test Status|Success|

### Test Case TC-4 : Start SUT With Unused Port And Full Access To Shared Resources As Parameters
|Test ID|TC-4|
|---|---|
|Test Name|Start SUT With Unused Port And Full Access To Chared Resources As Parameters|
|Test Description|Makes sure that SUT starts normally with normal starting conditions. This test case was re-written because the first version of it was marked with 'Defect' status (please check '3.2 Pass/Fail Criteria' in the test strategy document) because SUT asks for socket port number and shared resource container as parameters in an error message and then exits.|
|Test Data|Standard-Parameters|
|Test Classification (Priority/Severity)|Critical.|
|Pre-conditions|Make sure that only 'SUT.jar' exists in the current running folder and no residual files exist from a previous run. SUT is not running.|
|Test Steps|1 - Perform TC-3.|
||2 - Run SUT with parameters provided by test data.|
||3 - Perform TC-2 with 'Low' severity classification and make sure that the server has started as a __note__ (the __note__: that the server has started) for its test data.|
|Expected Results|1 - SUT starts a web server based on test data (port and path.)|
||2 - A console message that the server has started is displayed.|
||3 - TC-2 status is 'Success'.|
|Post-conditions|SUT has started a web server and is still running.|
|Actual Result|1 - SUT started a web server based on test data (port and path.)|
||2 - A console message that the server has started was displayed.|
||3 - TC-2 status is 'Fail'.|
|Test Status|Partially-Success|

### Test Case TC-5 : Start SUT With Used Port And Full Access To Shared Resources As Parameters
|Test ID|TC-5|
|---|---|
|Test Name|Start SUT With Used Port And Full Access To Shared Resources As Parameters|
|Test Description|Makes sure that SUT presents a message on the console stating that the provided port is previously taken. Please note that in the Requirements, the word 'socket' is used, and this test case assumes that the word 'socket' means 'port' here. Additionally, since the the port is provided as a paramere to the command line, this test case assumes that if SUT presents a message that the port is taken without specifically stating the port number, then it is considered as a 'success' if SUT presents the message immediatly after running SUT (and not wait until an HTTP request is invoked by a web browser or any other kind of client.)|
|Test Data|Standard-Parameters|
|Test Classification (Priority/Severity)|Critical.|
|Pre-conditions|Make sure that only 'SUT.jar' exists in the current running folder and no residual files exist from a previous run. SUT is not running.|
|Test Steps|1 - Perform TC-4.|
||2 - Run a second instance of SUT (other than the one run by TC-4) with parameters provided by test data.|
|Expected Results|Second SUT instance presents an error message that the port is taken, and then exits.|
|Post-conditions|The first instance of SUT (that is run by TC-4) is still in sunning state, and the second instance of SUT exits.|
|Actual Result|Second SUT instance has presented an error message that the port is taken, and then it has exited.|
|Test Status|Success|


---
# Test Report
