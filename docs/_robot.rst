..  code:: robotframework

    *** Settings ***

    Library  OperatingSystem
    Library  Selenium2Library
    Library  Selenium2Screenshots
    Library  String

    Suite Setup  Run keywords  Suite Setup
    Suite Teardown  Run keywords  Suite Teardown

    *** Variables ***

    ${START_PAGE}  https://google.com/
    @{DIMENSIONS}  1024  768
    ${BROWSER}     firefox

    *** Keywords ***

    Suite Setup
        Open browser  ${START_PAGE}  browser=${BROWSER}
        Set window size  @{DIMENSIONS}

    Suite Teardown
        Close all browsers

    *** Test Cases ***
