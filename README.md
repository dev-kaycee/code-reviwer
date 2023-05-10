# code-reviwer

Code Review Automation is a powerful tool for software development teams that want to streamline their code review process and ensure that their codebase is up to par.
This project involves creating an app that integrates with GitHub and Dropbox to automate the code review process.

## Here's how it works:

When a team member submits a code change to the GitHub repository, the app monitors the repository for changes.
When a change is detected, the app downloads the code changes from GitHub into a designated folder in Dropbox.
The app then runs tests and analysis on the code, using tools such as static code analysis and test suites, to identify potential issues or errors.
After the tests and analysis are complete, the app generates a report and provides feedback to the team, highlighting any issues or areas that require attention.
The team can then review the report and address any issues before merging the changes into the main branch of the codebase.
By automating the code review process, teams can save time and ensure that their code is of high quality. The integration with Dropbox also allows team members to access the code changes and review reports from anywhere, making it easier to collaborate on code review.

Overall, Code Review Automation can help software development teams to improve their code quality and streamline their code review process, ultimately leading to more efficient and effective software development.


# Configurations
### config.ymal
The YAML configuration file contains settings for integrating with  Dropbox and GitHub. 
The dropbox section specifies a single setting called token that should contain the access token for accessing a Dropbox account or API. The github section specifies two settings: token, which should contain the access token for accessing a GitHub account or API, and repository, which should specify the name of the repository on GitHub where files will be uploaded.

#### working_directory 
specify the directory on the local machine where files are stored before being uploaded to Dropbox and GitHub
#### test_directory
specify a separate directory where test files can be stored before being uploaded to Dropbox and GitHub.


"""
# setup.py

This script reads a YAML configuration file and creates a working directory and test directory based on the values specified in the configuration file.

Usage:
    python setup.py

Dependencies:
    - PyYAML

Configuration:
    The configuration file must be named "config.yml" and must be located in the same directory as the setup.py script. The following configuration options are supported:

    - working_directory: (string, optional) Specifies the path to the working directory where files will be stored before being uploaded to Dropbox and GitHub. If not specified, the working directory will not be created.
    
    - test_directory: (string, optional) Specifies the path to the test directory where test files will be stored before being uploaded to Dropbox and GitHub. If not specified, the test directory will not be created.
    
    - dropbox: (object, optional) Specifies the Dropbox settings. The following options are supported:
        - token: (string, required) Specifies the Dropbox access token for accessing a Dropbox account or API.

    - github: (object, optional) Specifies the GitHub settings. The following options are supported:
        - token: (string, required) Specifies the GitHub access token for accessing a GitHub account or API.
        - repository: (string, required) Specifies the name of the repository on GitHub where files will be uploaded.
"""

