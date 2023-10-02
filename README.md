# Automated-Testing-Challenge
        # DeepThought.robot -- File
        
*** Settings ***
Documentation       Suite Setup
Resource             ../../Resourses/UI/DeepThoughtStepdefinatio.robot

*** Test Cases ***
Verify User Login Page
        Test Successful Login With Valid Credentials
        Test Unsuccessful Login Attempts With Invalid Credentials



          # DeepThoughtStepdefination.robot  -- File

*** Settings ***
Documentation       Suite Setup
Library             SeleniumLibrary

*** Keywords ***
Test Successful Login With Valid Credentials
    open browser        https://dev.deepthought.education/login       chrome
    maximize browser window
    input text      //input[@id="username"]         Sejal Bhawsar
    input text      //input[@id="password"]         Pass123
    click button        //button[@id="login"]
    sleep           5s
    close browser

Test Unsuccessful Login Attempts With Invalid Credentials
    open browser        https://dev.deepthought.education/login     chrome
    maximize browser window
    input text          //input[@id="username"]         Sejal__Bhawsar
    input text          //input[@id="password"]         Pa ss 123
    click button        //button[@id="login"]
    sleep           5s
    close browser




