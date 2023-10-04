# Python

## concatenate lines from a text file
with open('file.txt') as inputfile:
    print ' '.join([line.rstrip('\n') for line in inputfile])

## Initial python file template


def main():
    print("Hello World!")

if __name__ == "__main__":
    main()

## Using requests with javascript
[From this article](https://thewebdev.info/2022/04/16/how-to-use-python-requests-with-javascript-pages/)

`from requests_html import HTMLSession

session = HTMLSession()
r = session.get('http://www.example.com')
r.html.render() `
