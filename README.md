# Web-vulnerabilities-scanner
A python 2.7 vulnerability scanner that can easily be customized to scan for specified vulnerabilities by replacing or adding strings to input fields. 

[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)

## Testing for application vulnerabilities
The vul_scanner.py will crawl and test input fields for XXS in links/forms and the simplest SQL injection of (password' or 1=1#) in forms. You should add more customized and complex inputs to make this program better. The input to test for vulnerability is stored as varibale and used as input to specified functions to test for vulnerabilities. This can easily be built upon. 

## Avoid getting logged out
Any inputs in the ```links_to_ignore``` variable in ```vul_scanner.py``` will be ignored. 

## Using credentials to crawl other otherwise inaccessible pages
Use the ```data_dict variable``` in ```vul_scanner.py``` to allow scanner to use credentials to gain access to pages specified in the ```vulnerabilities_scanner.session.post``` variable

## Running the program
Written in python 2.7, make sure to use the appropriate interrupter.
Specify the url in the ```target_url``` variable in ```vul_scanner.py```
To run the scanner
```bash
python vul_scanner.py
```

## 📈Example usage configurations
```python
#!usr/bin/env python

import scanner

target_url = "example.com"
links_to_ignore = ["example.com/logout/"]
# If initial scan scans a logout url, you'd want to include it in here so that you dont lose the post session

data_dict = {"username": "admin", "password": "password", "Login": "submit"}
# this is for if loggin in will get you more links and you know the login info

vulnerabilities_scanner = scanner.Scanner(target_url, links_to_ignore)
vulnerabilities_scanner.session.post("example.com/admin/login", data=data_dict) # this is the link to which the scanner will login and store as post

vulnerabilities_scanner.crawl()
vulnerabilities_scanner.run_scanner()
```

## Attention
Please do not use this program where unauthorized.

## Credits

|                                      |             |
| ------------------------------------ | ----------- |
| **Author**                           | @bryanwei   |

## License
See the [LICENSE](https://github.com/bryanweielio/Web-vulnerabilities-scanner/blob/master/LICENSE) file.
