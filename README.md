# Context-Automation-Framework
A Python automation framework built using Page-Object-Models &amp; Behave

Note: All packages assume a Linux OS and Python 3.5.2 (64bit)

1) Installing required packages

-Behave

    pip install behave

-Allure Behave formatter

    pip install allure-behave

-Selenium

    pip install selenium

- Allure
        
            sudo apt-add-repository ppa:qameta/allure
            sudo apt-get update 
            sudo apt-get install allure

    Note:
        If the above doesn't work, download Allure from https://github.com/allure-framework/allure-python and use ./Allure 
        
2) Running tests with Behave

    - NOTE: Navigate to your feature folder!

    - Behave (Standard)

          behave -D BROWSER=firefox UserRoles.feature 


    - Behave (Extended - Allure reporting - run behave with test output stored within allure-results)
        

            behave -f allure_behave.formatter:AllureFormatter -o allure-results/ -D BROWSER=firefox UserRoles.feature 


3) Viewing report
    - Navigate to Allures directory installation directory, if manually installed,
    else navigate to choosen custom output directory 
    
    Execute:
        - Navigate to Allure installation directory (if installed manually), else allure has been set within env path (remove './')
            
        ./allure generate /home/derp/Desktop/Context-Automation-Framework-master/features/allure-results/ --clean

        firefox index.html

