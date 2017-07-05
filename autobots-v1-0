#Autobots version 1.0
#Written by commandrine.
#Last updated on 22 Jun 2017.

# Ask for Protocol and store it in protocol
protocol = input('Enter HTTP or HTTPS: ')

# Ask for URL or IP and store it in domain
domain = input('Enter URL or IP: ')

robots = "/robots.txt"

from urllib.request import Request, urlopen
print('Checking "Robots.txt" for:')
print(domain)
print()
from urllib.error import URLError, HTTPError
req = Request(protocol+"://"+domain+robots)
try:
    response = urlopen(req)
except HTTPError as e:
    print('The server couldn\'t fulfill the request.')
    print('Error code: ', e.code)
except URLError as e:
    print('We failed to reach the server.')
    print('Reason: ', e.reason)
else:
    print('Contents of "Robots.txt" is as follows.')
    print()
with urlopen((protocol+"://"+domain+robots)) as stream:
    print(stream.read().decode("utf-8"))

