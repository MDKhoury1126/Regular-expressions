# Regular-expressions
import re

Fname = input('Enter file name')
if len(Fname) < 1:
    Fname = 'regex_sum_2406442.txt'

fh = open(Fname)
numbers = []

for line in fh:
    line = line.rstrip()
    found = re.findall('[0-9]+', line)
    for num in found:
        numbers.append(int(num))

print('Sum:', sum(numbers))
