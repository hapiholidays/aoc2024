# HapiHolidays Advent of Code 2024 GitHub Project

## Introduction
This is a project to implement solutions to (some of ) the Advent of Code 2024 puzzles in the language Hapi.

Hapi is a programming language unlike most other languages.
Where other languages may be defined around functions (like ML), objects (like C++) or even proof-searching (like Prolog), Hapi is defined around processes, and is based on the theory of the asynchronous pi-calculus and multiparty session types.

This means the solutions in Hapi should differ significantly from the solutions in Python, C++ etc. whic is why we believe it is a very interesting task to solve real world problems (or at least puzzles) in Hapi.

## Trying for yourself
It is relatively easy to run Hapi yourself. All it requires is a docker installation and following the steps below

1. Go to the project folder - this could be the "01" folder in a download or clone of this repository
2. Run the command (in a shell/terminal) `docker run -it -v ./:/project lassenielsen/hapi /bin/bash` to download (if you havent already) and start the docker image
3. Inside the docker image go to the project folder by typing `cd /project/`
4. Now you can build the solution to the first puzzle my typing `make sol1`
5. Finally you can run the built executable on the input file (assuming it is in the folder and called input.txt) by running `./sol1 input.txt` and it will (hopefully) solve the puzzle.
