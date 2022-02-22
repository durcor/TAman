# TAman
Scripts for making the life of a CS Teaching/Course Assistant (TA/CA) easier.

## Usage

### Do Once
- Make a `students.txt` file in the root of the class you grade for.

### Do Each Assignment
- Download all submissions for the assignment you want to grade from canvas to your downloads folder.
- Make a folder for the assignment and `cd` into it (ex: `cs420/hw/1`)
- Make or download test cases for the assignment in `tests.sh`
- Put the files needed in your solution to `sol/`
- Run `taman` to extract the submissions for your students.
- Run `grade` to grade the submissions.

## Example Directory Structure for your Class
```
└── cs420/
    ├── hw/
    │   ├── 1/ (populated by `taman` and `grade`)
    │   │   ├── grades/ (output by `grade`)
    │   │   │   ├── sandersonjohn.txt
    │   │   │   └── smithalice.txt
    │   │   ├── sol/ (solution files)
    │   │   │   ├── makefile
    │   │   │   └── main.c
    │   │   ├── tests.sh (test cases)
    │   │   └── subs/
    │   │       ├── sandersonjohn/
    │   │       │   ├── makefile
    │   │       │   └── main.c
    │   │       └── smithalice/
    │   │           ├── makefile
    │   │           └── main.c
    │   └── 2/ (before running anything)
    │       ├── sol/ (solution files)
    │       │   ├── makefile
    │       │   ├── first.c
    │       │   ├── third.c
    │       │   └── second.h
    │       └── tests.sh (test cases)
    └── students.txt (file with list of students you grade (name format: lastfirst) one per line)
```
