# Web-vulnerabilities-scanner
A python 2.7 vulnerability scanner that can easily be customized to scan for specified vulnerabilities by replacing or adding strings to input fields. 

## Getting Started
The vul_scanner.py will crawl and test input fields for XXS in links/forms and the simplest SQL injection of (password' or 1=1#) in forms. You should add more customized and complex inputs to make this program better. The input to test for vulnerability is stored as varibale and used as input to specified functions to test for vulnerabilities. This can easily be built upon. 

## Avoid getting logged out
Any inputs in the links_to_ignore variable in scanner.py will be ignored. 

## Using credentials to crawl other otherwise inaccessible pages
Use the data_dict variable in scanner.py to allow scanner to use credentials to gain access to pages specified in the vulnerabilities_scanner.session.post variable

## Running the program
Written in python 2.7, make sure to use the appropriate interrupter. 
Specify the url in the target_url variable in scanner.py
To run the scanner
python scanner.py

## Attention
Please do not use this program where unauthorized.

## Credits

|                                      |             |
| ------------------------------------ | ----------- |
| **Author**                           | @bryanwei   |

## License
See the [LICENSE](https://github.com/bryanweielio/Web-vulnerabilities-scanner/blob/master/LICENSE) file.
