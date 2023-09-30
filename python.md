# Python

## concatenate lines from a text file
with open('file.txt') as inputfile:
    print ' '.join([line.rstrip('\n') for line in inputfile])

## Initial python file template


def main():
    print("Hello World!")

if __name__ == "__main__":
    main()
