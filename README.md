![Supported Python versions](https://img.shields.io/badge/python-3.6+-blue.svg?style=flat-square&logo=python)
[![Go version](https://img.shields.io/badge/go-v1.16-blue)](https://golang.org/dl/#stable)
![License](https://img.shields.io/badge/license-GNU-green.svg?style=flat-square&logo=gnu)


# DomainRelationShips

```
██╗   ██╗ █████╗       ██╗██████╗                        
██║   ██║██╔══██╗      ██║██╔══██╗                       
██║   ██║███████║█████╗██║██║  ██║                       
██║   ██║██╔══██║╚════╝██║██║  ██║                       
╚██████╔╝██║  ██║      ██║██████╔╝                       
 ╚═════╝ ╚═╝  ╚═╝      ╚═╝╚═════╝                        
                                                         
██████╗  ██████╗ ███╗   ███╗ █████╗ ██╗███╗   ██╗███████╗
██╔══██╗██╔═══██╗████╗ ████║██╔══██╗██║████╗  ██║██╔════╝
██║  ██║██║   ██║██╔████╔██║███████║██║██╔██╗ ██║███████╗
██║  ██║██║   ██║██║╚██╔╝██║██╔══██║██║██║╚██╗██║╚════██║
██████╔╝╚██████╔╝██║ ╚═╝ ██║██║  ██║██║██║ ╚████║███████║
╚═════╝  ╚═════╝ ╚═╝     ╚═╝╚═╝  ╚═╝╚═╝╚═╝  ╚═══╝╚══════╝

> Get related domains / subdomains by looking at Google Analytics IDs
> Python/GO versions
> By @JosueEncinar
```

This script try to get related domains / subdomains by looking at Google Analytics IDs from a URL. First search for ID of Google Analytics in the webpage and then request to **builtwith** and **hackertarget** with the ID.

**Note**: It does not work with all websites.It is searched by the following expressions: 

```
->  "www\.googletagmanager\.com/ns\.html\?id=[A-Z0-9\-]+"
-> GTM-[A-Z0-9]+
->  "UA-\d+-\d+"
```

## Available versions:

* [Python](Python)
* [GO](GO)

## Installation:

Installation according to language.

### Python

```
> git clone https://github.com/Josue87/AnalyticsRelationships.git
> cd AnalyticsRelationships/Python
> sudo pip3 install -r requirements.txt
```

### GO

```
> git clone https://github.com/Josue87/AnalyticsRelationships.git
> cd AnalyticsRelationships/GO
> go build -ldflags "-s -w"
```

### Docker
```
> git clone https://github.com/Josue87/AnalyticsRelationships.git
> cd AnalyticsRelationships
> docker build -t analyticsrelationships:latest . 
```

## Usage

Usage according to language

### Python

```
> python3 analyticsrelationships.py -u https://www.example.com
```

Or redirect output to a file (banner or information messages are sent to the error output):

``` 
python3 analyticsrelationships.py -u https://www.example.com > /tmp/example.txt
```

### GO

```
>  ./analyticsrelationships --url https://www.example.com
```

Or redirect output to a file (banner or information messages are sent to the error output):

```
>  ./analyticsrelationships --url https://www.example.com > /tmp/example.txt
```

### Docker

```
>  docker run -it  analyticsrelationships:latest https://www.example.com
```

Or redirect output to a file (banner or information messages are sent to the error output):

```
>  docker run -it  analyticsrelationships:latest https://www.example.com > /tmp/example.txt
```
## Examples

### Python

Output redirection to file /tmp/example.txt:

![image](https://user-images.githubusercontent.com/16885065/118681597-fdf27180-b7ff-11eb-9b4d-c6738d1bc5ff.png)

Without redirection:

![image](https://user-images.githubusercontent.com/16885065/118681802-28442f00-b800-11eb-8a95-8b0de24ec691.png)

### GO

Without redirection:

![image](https://user-images.githubusercontent.com/16885065/118682807-0e571c00-b801-11eb-8da2-d9e3d3c1d555.png)

Working with file redirection works just like in Python.

# Author

This project has been developed by:

* **Josué Encinar García** -- [@JosueEncinar](https://twitter.com/JosueEncinar)


# Disclaimer!

This is a PoC. The author is not responsible for any illegitimate use.
