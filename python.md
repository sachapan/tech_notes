# Python

## concatenate lines from a text file
with open('file.txt') as inputfile:
    print ' '.join([line.rstrip('\n') for line in inputfile])
