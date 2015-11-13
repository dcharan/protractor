
Setting up your environment for node and Protractor
-------------
**Install Java and JavaJDK**. 
You need java jdk to be installed to get web driver and protractor running.

**Download and Install Node**
Goto  https://nodejs.org/en/

Confirm the installation by going to command prompt and type. Some users might have to open the command line in admin mode (for windows users only)
```
node -v
```
This should give your version of node installed on your machine. 

> **Info:**
Once you install node it would also install npm which is node package manager. (https://www.npmjs.com/). This is used to install external libraries

**Install Protractor module**
 Type the command in the command prompt. (https://angular.github.io/protractor/#/)

```
npm install -g protractor
```
 
> **Info:**
This will install two command line tools, **protractor** and **webdriver-manager**. 

**-g** after install is to tell npm to install protractor globally. 

Make sure protractor is installed by checking the version of protractor in the command line by typing

```
protractor --version 
```
This should print the version of protractor installed.

> **Tip:**
At any point if you want to what modules are installed then you could use this command
```
npm -g list 
```


Once you have installed protractor you should get webdriver manager. The webdriver-manager is a helper tool to easily get an instance of a Selenium Server running. 

Type the following command in the command prompt
```
webdriver-manager update
```
This should download the necessary binaries into your machine.

After the installation is done you could verify whether webdirver-manager is installed or not by typing 
 in the command prompt.

```
webdriver-manager 
```
You should see the location of the webdriver-manager and list of commands which you could use for webdriver-manager.

Now that you got protractor and webdriver-manager you should be able to start webdriver-manager by using the command in the command line
```
webdriver-manager start
```

If everything is good then you should see message like:
```
INFO - RemoteWebDriver instances should connect to: http://127.0.0.1:4444/wd/hub
INFO - Selenium Server is up and running.
```
If you see the about message then if you go to url http://127.0.0.1:4444/wd/hub from the browser then you should see Sessions.

**webdriver manager start issue**

if you see any error related to 
```
"seleniumProcess.pid: undefined" 
```
Then open the command prompt in administrator mode. and run the 
```
webdriver-manager start
```
Now that we have installed everything required for protractor we should be able to run the tests.  

> **CAUTION:**
CAUTION: Chrome version must be >= 43.0.2357.0

